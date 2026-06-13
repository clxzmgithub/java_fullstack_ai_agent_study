# MCP 协议学习笔记

> 知识来源：JavaGuide AI Agent 系列文章学习整理
> 关联文档：`mcp.md`、`agent-basis.md`、`harness-engineering.md`

---

## 一、MCP 是什么

**MCP（Model Context Protocol）** = 模型上下文协议，是一套**通信协议规范**。

把 MCP 全称拆开来看：
- **Model**：面向大模型应用
- **Context**：把外部上下文、工具和数据源带给模型
- **Protocol**：用一套标准协议把交互方式定下来

### 核心价值一句话

> **MCP 让工具接入从"各自适配"变成"统一接口"。**

没有 MCP 时，每个 AI 应用（Cursor、Claude Desktop、自研 Agent）都要各自维护一套"怎么连工具"的方式。MCP 定了一套标准：工具提供方封成 MCP Server，任何支持 MCP 的 AI 应用连上来，就能自动发现并调用这些工具。

### 类比
- MCP ≈ HTTP 协议（通信规范）
- MCP Server ≈ Web 服务器（实现了协议的服务程序）
- MCP Client ≈ 浏览器（发请求的一方）
- Host（Claude Desktop/Cursor）≈ 用浏览器上网的人

---

## 二、核心角色：Host / Client / Server

```
用户
  ↓
Host（AI 应用：Claude Desktop / Cursor / 自研 Agent 平台）
  ↓ 内含
MCP Client（负责和 MCP Server 通信）
  ↓ JSON-RPC 2.0
MCP Server（封装了具体能力的服务程序）
  ↓
Data Source（数据库、文件、第三方 API、内部系统）
```

- **Host**：用户面对的 AI 应用本体，负责承载用户交互和模型调用
- **Client**：Host 内部负责和 Server 通信的那一层（通常不需要自己写）
- **Server**：开发者最常接触的部分，把能力封装后通过 MCP 协议暴露出去

> 一个 Host 可以同时连接多个 MCP Server。

---

## 三、MCP 三类标准原语

**原语（Primitive）**：不可再分割的最小功能单元，是系统对外暴露能力的最基础分类。

> **核心区分维度：谁来用，怎么用。**

### 🔧 Tools（可执行动作）

- **定性**：模型主动调用，会改变外部世界（或触发真实操作）
- **关键词**：主动 + 可执行 + 有副作用
- **例子**：
  - `query_slow_sql(service_name, time_range)` → 查慢 SQL 日志
  - `get_cpu_metrics(service_name, time_range)` → 查 CPU 指标
  - `send_report(channel, content)` → 发报告到 Slack
- **谁决定调用**：模型根据推理自主判断要不要调

---

### 📄 Resources（只读上下文数据）

- **定性**：给模型"看"的，不是让模型"做"的
- **关键词**：被动 + 只读 + 提供上下文
- **例子**：
  - 服务依赖拓扑图（order-service 依赖哪些下游）
  - 数据库 Schema（orders 表有哪些字段、哪些有索引）
  - 告警规则配置
  - 本地文件内容、日志片段
- **作用**：模型读了之后，知道背景信息，然后结合这些上下文去推理或生成
- **谁决定加载**：通常由 Host、用户界面或应用逻辑决定

---

### 📋 Prompts（可复用提示词模板）

- **定性**：把固定任务的做法沉淀下来，按需调用
- **关键词**：模板 + 复用 + 固定流程
- **例子**：
  - "按团队规范做代码审查"的完整提示词
  - "生成故障复盘初稿"的结构化模板
  - "把接口文档整理成测试用例"的标准流程
- **谁决定触发**：用户点按钮 / 输入斜杠命令 / 程序逻辑自动注入

---

### 用"凉拌黄瓜"类比三类原语

| 原语      | 对应场景                            | 角色                     |
|-----------|-------------------------------------|--------------------------|
| Resources | 冰箱里有什么、有没有黄瓜、调料在哪  | 食材和菜谱（给厨师看的）  |
| Tools     | 切菜、拌料、下单买菜                | 具体的动作               |
| Prompts   | 家里固定偏好：少放辣、必须加香菜    | 任务规则模板             |

---

### 三类原语的对比表

| 维度       | Tools          | Resources      | Prompts            |
|------------|----------------|----------------|--------------------|
| 有无副作用 | ✅ 有          | ❌ 无（只读）  | ❌ 无              |
| 谁来触发   | 模型自主判断   | Host/程序逻辑  | 用户/Host/程序逻辑 |
| 核心用途   | 执行真实操作   | 提供背景知识   | 标准化任务做法     |
| 类比       | 员工的手       | 员工的眼睛     | 操作手册           |

---

## 四、MCP 三类原语 vs Harness 六层架构（L2）

**MCP 是 L2 工具系统层的标准接入协议。**

| MCP 原语 | 在 L2 里的定位 | 具体作用 |
|----------|---------------|----------|
| **Tools** | L2 的**核心执行单元** | 驱动 Agent Loop 转起来，产生真实动作，结果回传形成反馈闭环 |
| **Resources** | L2 的**上下文补充输入** | 工具调用前，给模型提供背景数据，让模型选对工具、填对参数 |
| **Prompts** | L2 与 **L1（信息边界层）的交界** | 规范工具使用方式，固化任务流程 |

> L2 定义了"需要什么能力"，MCP 提供了标准化方式来实现它。两者是**架构设计与工程实现**的关系。

---

## 五、MCP Server 代码示例（Python）

```python
from mcp.server.fastmcp import FastMCP

mcp = FastMCP("weather-server")

# 声明一个 Tool（可执行动作）
@mcp.tool()
def get_weather(city: str) -> str:
    """获取指定城市的天气信息"""
    return f"{city} 今天晴天，温度 25°C"

# 声明一个 Resource（只读数据）
@mcp.resource("weather://forecast")
def weather_forecast() -> str:
    """返回未来一周天气预报"""
    return "未来七天天气预报..."

# 声明一个 Prompt（可复用模板）
@mcp.prompt()
def weather_report_template() -> str:
    """生成天气播报的标准格式"""
    return "请按以下格式播报天气：今日{city}，{weather}，温度{temp}..."

if __name__ == "__main__":
    mcp.run()
```

**三种装饰器 `@mcp.tool`、`@mcp.resource`、`@mcp.prompt` 对应三类原语。**

Server 启动后，MCP Client 连上来初始化握手，问"你有什么能力"，Server 回答工具/资源/提示词列表，双方确认后进入可用状态。

---

## 六、一次完整 MCP 调用流程

```
用户提问
  ↓
Host 把 [可用工具列表 + 用户消息] 一起发给大模型
  ↓
大模型推理，用 Function Calling 输出结构化意图：
  {"name": "get_weather", "arguments": {"city": "北京"}}
  ↓
Host 里的 MCP Client 按 JSON-RPC 2.0 协议发请求：
  POST /mcp
  {"jsonrpc": "2.0", "method": "tools/call", "params": {"name": "get_weather", ...}}
  ↓
MCP Server 执行 get_weather 函数，返回结果
  ↓
结果回传给模型，模型组织自然语言回答
```

---

## 七、Client 侧能力（进阶）

除了 Server 暴露三类原语，Client 也可以提供能力给 Server 使用：

| 能力          | 说明                                                         |
|---------------|--------------------------------------------------------------|
| **Roots**     | Host 告诉 Server："你只能在这些文件目录范围内工作"           |
| **Sampling**  | Server 请求 Host 侧的 LLM 做一次生成（如日志摘要）           |
| **Elicitation** | Server 执行时向用户补充询问信息（参数不完整时弹出交互）    |

> 大多数 MCP Server 一开始只用 Tools 就够了，后面按需补充。

---

## 八、传输方式选择

| 场景                             | 推荐传输方式    |
|----------------------------------|-----------------|
| 本地工具、本地文件、个人使用     | **stdio**       |
| 团队服务、远程 API、多用户访问   | **Streamable HTTP** |

**stdio 注意事项**：
- 不要往 stdout 打调试日志！stdout 是 JSON-RPC 消息通道，随手 `print()` 就会污染消息流导致 Server 断连
- 日志应写到 **stderr 或文件**

---

## 九、工具描述怎么写才有效

模型选不选对工具，依据**只有 description**，没有别的。

```python
# ❌ 差的描述（太模糊，模型不知道什么时候用）
@mcp.tool()
def get_data(type: str, id: str) -> str:
    """获取数据"""
    ...

# ✅ 好的描述（说清楚使用场景 + 禁用场景）
@mcp.tool()
def query_slow_sql(service_name: str, time_range: str) -> str:
    """
    查询慢 SQL 日志，适用于：服务响应慢、数据库超时、CPU 飙升且怀疑和数据库有关时。
    如果用户问的是网络问题或内存问题，不要调用这个工具。
    """
    ...
```

**好的描述三要素**：
1. 什么时候该用（使用场景）
2. 需要哪些参数（参数含义）
3. 什么时候不要用（禁用场景）

---

## 十、生产环境上 MCP 的注意事项

| 问题         | 要点                                                       |
|--------------|------------------------------------------------------------|
| Schema 管理  | 字段单位、时间格式、枚举值、默认值要写清楚；要有版本号     |
| 权限安全     | 区分只读/写操作；防路径遍历、SQL 注入；高危操作人工确认    |
| 可观测性     | 每次调用要有 Trace ID；结构化日志记录参数、耗时、错误码    |
| 成本归因     | 能按用户、业务线、工具拆分统计 Token 和 API 成本           |
| 工具粒度     | 不要封"万能工具"；拆小一点，权限更清晰，模型判断更准确     |
| 大文件处理   | 先返回元数据，再分块读取，设置硬限制（如单资源不超过 10MB）|

---

## 十一、核心认知总结

1. **MCP 解决"工具接入碎片化"**，不是让模型更聪明，也不替代 Function Calling
2. **三类原语**：Tools（执行动作）、Resources（只读数据）、Prompts（任务模板）
3. **MCP 是 L2 工具系统层的实现协议**，L2 定义要做什么，MCP 提供标准化方式
4. **工具描述质量直接决定 Agent 表现**，描述写错了模型就选错工具
5. **Demo 能跑 ≠ 可以上生产**，权限、可观测性、版本管理一个都不能少

