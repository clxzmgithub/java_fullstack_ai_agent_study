# 📚 Java 后端 & 全栈 & AI & Agent 应用开发学习项目

<div align="center">

![Status](https://img.shields.io/badge/状态-持续更新中-brightgreen)
![License](https://img.shields.io/badge/license-MIT-blue)
![Java](https://img.shields.io/badge/Java-17%2B-orange)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.x-green)

</div>

---

## 📌 项目定位

本项目是一个面向**工程实践**的系统性学习仓库，**不是真实的生产项目**。聚焦于 Java 全栈工程化体系的深度实践，横跨后端架构、分布式系统、大数据生态、数据分析、风控与爬虫、前端、多语言拓展、AI/Agent 应用开发等方向，以动手实验、场景设计、面试题解析为主要学习载体，逐步构建完整的全栈工程师知识体系。

**核心学习方向（15 大板块）：**
`Spring 全家桶` · `数据库与存储` · `消息队列` · `分布式系统` · `架构设计` · `系统设计与面试题` · `稳定性保障` · `网络与通信` · `认证授权与安全` · `容器与云原生` · `大数据生态` · `数据分析` · `爬虫·逆向·反爬·风控` · `多语言拓展 + 前端` · `AI 算法理论 + AI/Agent 开发`

> ⚠️ **关联项目分工说明**
>
> 本人维护三个相互补充、各有侧重的学习仓库，共同构成完整的知识体系：
>
> | 项目 | 定位 | 核心聚焦 |
> |------|:----:|---------|
> | [`java_study`](../java_study) | 🔵 基础理论 | Java 语言核心、数据结构与算法、JVM 原理、操作系统、计算机网络——**打地基** |
> | **本项目**（`java_fullstack_ai_agent_study`） | 🟠 工程实践 | Spring 生态、分布式架构、大数据、存储中间件、风控爬虫、数据分析、多语言、AI/Agent——**做系统** |
> | [`ai_coding_harness_engineering_study`](../ai_coding_harness_engineering_study) | 🟣 AI 工程 | AI 编程方法论、上下文工程、Harness 理论、AI Coding 工具链、大模型与 Agent 开发——**用 AI 提效** |

---

## 🗺️ 技术版图

### 🧩 Spring 全家桶
| 技术 | 学习要点 |
|------|---------|
| Spring Framework | IoC / AOP / 事件机制 / Bean 生命周期 |
| Spring Boot | 自动装配原理 / Starter 开发 / 配置体系 |
| Spring MVC | 请求处理链 / 过滤器 / 拦截器 |
| Spring Cloud | Nacos / Gateway / OpenFeign / Sleuth / Config |
| Spring Security | 认证授权流程 / RBAC 模型 / OAuth2 资源服务器 |
| Spring Data | JPA / Redis / ES 集成 |
| Spring Batch | 批处理架构 / Job & Step 设计 |

### 🗄️ 数据库与存储
| 技术 | 学习要点 |
|------|---------|
| MySQL | SQL 优化 / 索引原理 / 事务与锁 / 主从复制 / 分库分表 |
| Redis | 数据结构 / 持久化 / 集群模式 / 缓存策略 / 分布式锁 |
| Elasticsearch | 全文检索 / 索引设计 / 聚合分析 / 与 MySQL 数据同步 |
| MongoDB | 文档模型 / 适用场景 / 性能调优 |
| HBase | 大宽表设计 / RowKey 设计 / 与 Hadoop 生态集成 |

### 📨 消息队列
| 技术 | 学习要点 |
|------|---------|
| Kafka | 生产消费模型 / 分区设计 / 幂等与事务消息 / 消息积压处理 / 与 Spring 集成 |

### 🔧 构建与工程化
| 技术 | 学习要点 |
|------|---------|
| Git | 分支策略 / Rebase vs Merge / Hooks / 大仓管理 |
| Gradle | 多模块构建 / 依赖管理 / 自定义 Task / 增量构建 |
| Maven | 生命周期 / 插件机制 / 私服搭建 / 多模块继承 |

### 🌐 网络与通信
| 技术 | 学习要点 |
|------|---------|
| Netty | NIO/BIO/AIO 对比 / 事件循环 / Pipeline / 自定义协议 / 长连接管理 |
| RPC | gRPC / Dubbo / Thrift 原理 / 服务注册与发现 |
| CDN | 内容分发原理 / 回源策略 / 静态资源加速 |

### 🔐 认证授权与安全
- **登录体系**：Session / JWT / OAuth2 / SSO 单点登录 / 无感刷新 Token
- **认证授权**：RBAC / ABAC 模型、Spring Security 深度集成
- **安全加固**：XSS / CSRF / SQL 注入防御 / 接口签名 / 数据脱敏

### ⚙️ 分布式系统
- **ZooKeeper**：选举机制 / 分布式协调 / 配置中心 / 分布式锁
- **分布式理论**：CAP / BASE / Paxos / Raft 一致性算法
- **分布式事务**：2PC / TCC / Saga / 消息最终一致性

### 🏗️ 架构设计与系统设计

#### 三高架构
| 方向 | 学习要点 |
|------|---------|
| 高性能 | 连接池调优 / 线程模型 / 异步化 / JVM GC 调优 / 缓存架构 / 读写分离 |
| 高可用 | 多活架构（同城双活/异地多活）/ 容灾备份 / 故障演练 / SLA 保障 / 无状态设计 |
| 高扩展 | 水平扩展 / 垂直扩展 / 分层架构 / 插件化设计 / 开闭原则落地 |

#### 架构设计方法论
- **系统设计方法论**：需求拆解 / 容量估算 / 核心组件选型 / Back-of-envelope 估算
- **负载均衡**：L4/L7 负载均衡 / Nginx / LVS / 一致性哈希
- **DDD 领域驱动设计**：战略设计（限界上下文 / 领域 / 子域）/ 战术设计（实体 / 值对象 / 聚合根 / 领域事件 / 仓储）
- **业务架构**：业务建模 / 服务划分原则 / 微服务 vs 单体权衡 / 事件风暴（Event Storming）
- **常见架构模式**：CQRS / Event Sourcing / Saga / Outbox Pattern / Strangler Fig

### 🛡️ 稳定性保障
| 方向 | 技术与方案 |
|------|-----------|
| 限流 | 令牌桶 / 漏桶算法 / Sentinel / Redis 限流 |
| 熔断降级 | Hystrix / Resilience4j / 服务降级策略 |
| 幂等性 | Token 机制 / 数据库唯一键 / Redis 去重 |
| 冗余 | 数据冗余 / 服务多副本 / 异地多活 |

### 🐳 容器与云原生
- **Docker**：镜像构建 / 网络模型 / Volume 管理
- **Kubernetes**：Pod / Service / Ingress / HPA / 滚动发布
- **Crane**：美团内部容器调度平台实践

### 🌍 多语言拓展

> 💡 汇编与 C/C++ 作为最接近硬件的底层语言，是理解计算机体系结构、性能优化与系统编程的基石，即便暂不深入，也值得保持敬畏与了解。

| 语言 | 优先级 | 学习要点 |
|------|:------:|---------|
| Go | 🔥 高 | 语法特性 / Goroutine & Channel / Gin / Gorm / 与 Java 对比 |
| Python | 🔥 高 | FastAPI / 数据处理 / 脚本自动化 / 与 Java 互调 |
| Node.js | 🔥 高 | 事件循环原理 / NestJS / BFF 层设计 / 全栈场景 |
| Shell | 🟡 中 | Bash 语法 / 变量与流程控制 / 正则 / 常用命令组合 / 自动化脚本 |
| C / C++ | 🔵 了解 | 指针与内存管理 / 编译链接原理 / 标准库 / 系统调用基础 |
| 汇编语言 | 🔵 了解 | 寄存器与指令集（x86/ARM）/ 栈帧结构 / 与高级语言的对应关系 |

### 🖥️ 前端技术
- **基础**：HTML5 / CSS3 / JavaScript（ES6+）/ TypeScript
- **框架**：React / Vue3 核心原理与工程实践
- **工程化**：Webpack / Vite / 前后端联调 / RESTful & GraphQL API 设计

### 🐘 大数据生态
| 技术 | 学习要点 |
|------|---------|
| Hadoop | HDFS 架构 / MapReduce 编程模型 / YARN 资源调度 |
| Hive | HQL / 分区与分桶 / 存储格式（ORC/Parquet）/ 执行引擎（Tez/Spark）|
| Spark | RDD / DataFrame / SparkSQL / Spark Streaming / 调优 |
| Flink | 流批一体 / 事件时间与窗口 / 状态管理 / Checkpoint / Table API |
| Presto / Trino | 联邦查询 / OLAP 即席分析 |
| 数据湖 | Delta Lake / Apache Iceberg / Hudi 对比与选型 |
| 数据仓库 | 分层架构（ODS/DWD/DWS/ADS）/ 数据建模（星形/雪花模型）|
| 数据治理 | 元数据管理 / 数据血缘 / 数据质量 / Apache Atlas |

### 🧠 AI 算法理论

> 💡 机器学习、深度学习是当下 AI 浪潮的核心基础，即便不从事算法岗位，理解其原理有助于更好地使用和评估 AI 能力，是工程师认知升级的重要拼图。

| 方向 | 学习要点 |
|------|---------|
| 机器学习基础 | 监督 / 无监督 / 强化学习 / 特征工程 / 模型评估（偏差-方差）|
| 神经网络 | 前向传播 / 反向传播 / 激活函数 / 损失函数 / 梯度下降 |
| 深度学习 | CNN / RNN / LSTM / Attention 机制 / Transformer 架构 |
| 大模型原理 | Pre-training / SFT / RLHF / Scaling Law / MoE 架构 |
| AI 框架 | PyTorch / TensorFlow / HuggingFace Transformers / ModelScope |
| 大模型生态 | OpenAI API / Claude / Gemini / Qwen / LLaMA / DeepSeek |

### 🎯 面试题与真实场景设计

> 💡 结合真实互联网场景，将技术知识融入实战，是查漏补缺、深化理解的最佳路径。

| 方向 | 内容 |
|------|------|
| 系统设计场景题 | 设计短链系统 / 设计秒杀系统 / 设计消息推送系统 / 设计Feed流 / 设计搜索系统 |
| 分布式场景题 | 分布式 ID 生成 / 分布式锁方案对比 / 分布式事务选型 / 一致性方案设计 |
| 数据库场景题 | 大表优化 / 分库分表方案 / 缓存与数据库一致性 / 慢查询排查 |
| 高并发场景题 | 接口幂等设计 / 限流方案选型 / 热点数据处理 / 流量削峰填谷 |
| 真实互联网面试题 | 美团 / 阿里 / 字节 / 腾讯等大厂高频后端面试题整理与解析 |
| 架构面试题 | 三高系统设计 / DDD 落地 / 微服务拆分实践 / 技术选型决策 |

### 🕷️ 爬虫、逆向与反爬

> 💡 爬虫与逆向是数据采集、竞品分析、安全研究的核心技能；反爬则是保护自身数据资产的重要手段。三者与风控共同构成进攻防守的完整体系。

#### 🐛 爬虫技术
| 方向 | 学习要点 |
|------|---------|
| 爬虫基础 | HTTP 协议详解 / Request 伪装 / Cookie & Session 管理 / 代理池 |
| 爬虫框架 | Scrapy（Python）/ Playwright / Puppeteer / Selenium / Jsoup（Java）|
| 分布式爬虫 | 任务调度 / 去重 / 增量爬取 / 爬虫集群幻化 |
| 数据解析 | XPath / CSS Selector / 正则表达式 / JSON 解析 |
| JS 渲染页爬取 | Headless 浏览器 / 动态页面处理 / 等待策略 |

#### 🔐 逆向工程
| 方向 | 学习要点 |
|------|---------|
| 抓包分析 | Fiddler / Charles / Wireshark / mitmproxy 抓包工具实战 |
| JS 逆向 | JS 混淆还原 / AST 解析 / Hook 技术 / 加密算法还原 |
| App 逆向 | APK 反编译（jadx / apktool）/ 抓包分析 / 小程序逆向 |
| 协议分析 | 请求签名算法还原 / Token 机制分析 / 加密参数破解 |
| 环境条件分析 | 判断架 / Root 检测 / 模拟器检测 / SSL Pinning 绕过 |

#### 🛡️ 反爬系统设计
| 方向 | 学习要点 |
|------|---------|
| 基础防护 | IP 限流 / User-Agent 检测 / Referer 验证 / 请求频率控制 |
| 验证码与行为识别 | 图形验证码 / 滑块验证 / 指纹识别（字体 / 画布 / WebGL）|
| AI 反爬 | 机器行为建模 / 异常访问模式识别 / 风控分 |
| 设备指纹 | 浏览器指纹收集 / TLS 指纹 / 网络行为特征 |
| 防爬系统设计 | 多层防护架构 / 实时风控决策 / 蛮蜂罐 / 开放接口签名 |

### 🔰 风控系统

> 💡 风控是爬虫对抗、反欺诈、账号安全的核心引擎，与爬虫/逆向/反爬深度关联。大厂（美团、阿里、字节等）的风控体系都是高价值学习样本。

#### 🎯 业务风控
| 方向 | 学习要点 |
|------|---------|
| 账号安全 | 撞库检测 / 账号盗用识别 / 异常登录判断 / 设备绑定策略 |
| 交易风控 | 支付欺诈识别 / 异常下单检测 / 黑产对抗 / 羊毛党识别 |
| 内容风控 | 垃圾内容过滤 / 违禁词检测 / 用户举报处理 / AI 审核 |
| 活动风控 | 优惠券滥用 / 刷单检测 / 营销作弊 / 新人红包对抗 |
| 爬虫风控 | Bot 检测 / 接口滥用识别 / 数据爬取防护 |

#### 🧩 风控核心技术
| 方向 | 学习要点 |
|------|---------|
| 规则引擎 | 规则配置 / 动态规则热更新 / 规则优先级 / Drools / 自研规则引擎 |
| 设备指纹 | 浏览器指纹 / App 设备指纹 / 设备标识生成与存储策略 |
| 行为序列分析 | 用户行为序列建模 / 异常行为识别 / 操作路径分析 |
| 图谱风控 | 关联图谱（账号/设备/IP/手机号）/ 团伙欺诈识别 / 图神经网络应用 |
| AI 风控模型 | 特征工程 / 有监督/无监督模型 / 实时推理 / 模型迭代 |
| 实时风控架构 | 同步风控 vs 异步风控 / 毫秒级决策 / Flink 实时计算 / 规则 + 模型融合 |

#### 🏗️ 风控系统设计
| 方向 | 学习要点 |
|------|---------|
| 风控系统架构 | 前置拦截 / 事中监控 / 事后审计 / 分层决策体系 |
| 名单系统 | 黑/白/灰名单管理 / 名单同步 / TTL 策略 / 联邦名单 |
| 事件总线 | 风控事件上报 / 异步处理 / Kafka 接入 / 事件溯源 |
| 案例系统 | 可疑事件案例化 / 人工审核工作台 / 风控闭环 |
| 风控度量 | 误判率 / 漏判率 / ROC/AUC / 风控效果评估体系 |

### 📊 数据分析

> 💡 数据分析是从数据中提炼业务洞察的关键能力，包含指标体系设计、可视化表达、用户行为分析、A/B 实验等。对后端工程师而言，理解数据分析能够帮助更好地设计数据采集、埋点与指标体系。

#### 📏 指标与埋点体系
| 方向 | 学习要点 |
|------|---------|
| 指标体系设计 | 北极星 / OKR / 核心指标拆解 / 北极星指标 vs 过程指标 |
| 埋点设计 | 埋点规范 / 事件分类 / 属性设计 / 埋点 SDK 集成 |
| 数据采集 | 前端埋点 / 后端埋点 / 日志采集 / 第三方数据接入 |
| 数据质量治理 | 埋点准确性校验 / 数据对账 / 异常表现监控 |

#### 🔍 分析方法与模型
| 方向 | 学习要点 |
|------|---------|
| 用户路径分析 | 漏斗模型 / 路径分析 / 转化漏斗分析 |
| 留存与活跃分析 | DAU/MAU / 用户留存率 / 活跃度分层 / Cohort 分析 |
| 用户分群 | RFM 模型 / 用户标签体系 / 用户生命周期分析 |
| 归因分析 | 同环比 / 环比 / 指标异常归因方法论 / 归因树 |
| A/B 实验 | 实验设计 / 分流策略 / 显著性检验 / 多层分流 / Holdout 组 |
| 预测分析 | 时序预测 / 用户行为预测 / 模型评估 / 特征重要性 |

#### 🛠️ 分析工具与平台
| 方向 | 学习要点 |
|------|---------|
| SQL 分析 | 窗口函数 / 常用分析模式 / 复杂查询优化 |
| Python 数据分析 | Pandas / NumPy / Matplotlib / Seaborn / 数据清洗与转换 |
| 可视化 | Tableau / Superset / Grafana / ECharts / 数据看板设计原则 |
| 分析平台 | 实时 OLAP（Doris/ClickHouse）/ 役角分析（分析师 vs 开发）|
| 增长分析框架 | AARRR 模型 / HEART 框架 / 北极星指标 / 第一核心行动 |

### 🤖 AI 与 Agent 应用开发
| 方向 | 学习要点 |
|------|---------|
| 大模型应用 | Prompt 工程 / RAG 检索增强生成 / Fine-tuning 基础 |
| Agent 框架 | LangChain / LangGraph / AutoGen / ReAct 模式 |
| AI 工程化 | 向量数据库（Milvus/Chroma）/ 模型部署 / 推理优化 |
| Java AI 集成 | Spring AI / 模型调用封装 / Function Calling |

---

## 📁 项目结构

> 🚧 目录结构规划中，随学习进度逐步创建与完善。

```
java_fullstack_ai_agent_study/
├── README.md                    # 项目总览（当前文件）
│
├── spring/                      # Spring 全家桶实践
│   ├── spring-core/             #   IoC / AOP 实验
│   ├── spring-boot/             #   自动装配 / Starter 开发
│   ├── spring-cloud/            #   微服务体系
│   └── spring-security/         #   认证授权
│
├── databases/                   # 数据库与存储
│   ├── mysql/                   #   SQL 优化 / 事务 / 分库分表
│   ├── redis/                   #   数据结构 / 集群 / 分布式锁
│   ├── elasticsearch/           #   全文检索 / 聚合
│   ├── mongodb/                 #   文档模型
│   └── hbase/                   #   大宽表设计
│
├── messaging/                   # 消息队列
│   └── kafka/                   #   生产消费 / 事务消息
│
├── network/                     # 网络与通信
│   ├── netty/                   #   自定义协议 / 长连接
│   └── rpc/                     #   gRPC / Dubbo
│
├── security/                    # 认证授权与安全
│   ├── jwt-oauth2/
│   └── sso/
│
├── distributed/                 # 分布式系统
│   ├── zookeeper/
│   └── distributed-transaction/
│
├── architecture/                # 架构设计
│   ├── three-high/              #   三高架构（高性能/高可用/高扩展）
│   ├── ddd/                     #   DDD 领域驱动设计
│   ├── business-arch/           #   业务架构 / 服务划分 / 建模
│   └── arch-patterns/           #   CQRS / Event Sourcing / Saga 等
│
├── system-design/               # 系统设计案例
│   ├── scenarios/               #   真实场景设计题（短链/秒杀/Feed流等）
│   └── interview-questions/     #   大厂高频面试题整理
│
├── high-performance/            # 高性能 / 高可用
│
├── stability/                   # 稳定性（限流 / 熔断 / 幂等）
│
├── cloud-native/                # 容器与云原生
│   ├── docker/
│   └── kubernetes/
│
├── build-tools/                 # 构建工具
│   ├── gradle/
│   └── maven/
│
├── other-languages/             # 多语言拓展
│   ├── go/
│   ├── python/
│   ├── nodejs/
│   ├── shell/                   #   Bash 脚本 / 自动化
│   ├── c-cpp/                   #   C/C++ 基础 / 内存 / 系统调用
│   └── assembly/                #   汇编指令集 / 与高级语言映射
│
├── frontend/                    # 前端技术
│   ├── react/
│   └── vue/
│
├── big-data/                    # 大数据生态
│   ├── hadoop/                  #   HDFS / MapReduce / YARN
│   ├── hive/                    #   数仓 HQL / 存储格式
│   ├── spark/                   #   RDD / SparkSQL / Streaming
│   ├── flink/                   #   流批一体 / 状态管理
│   ├── data-warehouse/          #   数仓分层设计 / 建模
│   └── data-governance/         #   数据治理 / 血缘 / 质量
│
├── data-analysis/               # 数据分析
│   ├── metrics-tracking/        #   指标与埋点体系
│   ├── analysis-methods/        #   分析方法 / A/B实验 / 用户分群
│   └── tools/                   #   SQL / Python / 可视化工具
│
├── ai-algorithm/                # AI 算法理论
│   ├── machine-learning/        #   机器学习基础
│   ├── deep-learning/           #   神经网络 / CNN / RNN / Transformer
│   └── llm-theory/              #   大模型原理 / RLHF / MoE
│
├── crawler-reverse/             # 爬虫、逆向与反爬
│   ├── crawler/                 #   爬虫基础 / 分布式爬虫 / JS渲染
│   ├── reverse/                 #   抓包分析 / JS逆向 / App逆向
│   └── anti-crawler/            #   反爬系统设计 / 风控 / 指纹
│
├── risk-control/                # 风控系统
│   ├── business-risk/           #   账号/交易/内容/活动风控
│   ├── rule-engine/             #   规则引擎 / Drools
│   ├── device-fingerprint/      #   设备指纹体系
│   ├── graph-risk/              #   图谱风控 / 团伙识别
│   └── realtime-arch/           #   实时风控架构设计
│
└── ai-agent/                    # AI 与 Agent 应用开发
    ├── rag/
    ├── langchain/
    └── spring-ai/
```

---

## 📊 学习进度

> 各模块学习状态持续更新。状态说明：🔜 待开始 ｜ 🔥 进行中 ｜ ✅ 已完成 ｜ ⏸️ 暂停

<table>
  <thead>
    <tr>
      <th>主模块</th>
      <th>子模块</th>
      <th>状态</th>
      <th>备注</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="5"><b>🧩 Spring 全家桶</b></td>
      <td>Spring Framework（IoC / AOP / 事件机制）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>Spring Boot（自动装配 / Starter 开发）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>Spring Cloud（Nacos / Gateway / OpenFeign / Sleuth）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>Spring Security / OAuth2 资源服务器</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>Spring Data / Batch</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td rowspan="5"><b>🗄️ 数据库与存储</b></td>
      <td>MySQL（索引 / 事务与锁 / 主从复制 / 分库分表）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>Redis（数据结构 / 持久化 / 集群 / 分布式锁）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>Elasticsearch（全文检索 / 索引设计 / 聚合分析）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>MongoDB（文档模型 / 适用场景）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>HBase（大宽表设计 / RowKey 设计）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td rowspan="1"><b>📨 消息队列</b></td>
      <td>Kafka（生产消费 / 分区设计 / 事务消息 / 积压处理）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td rowspan="3"><b>🌐 网络与通信</b></td>
      <td>Netty（NIO/BIO/AIO / 自定义协议 / 长连接管理）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>RPC（gRPC / Dubbo / Thrift / 服务注册与发现）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>CDN（内容分发原理 / 回源策略）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td rowspan="3"><b>🔐 认证授权与安全</b></td>
      <td>登录体系（Session / JWT / OAuth2 / SSO 单点登录）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>认证授权（RBAC / ABAC 模型）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>安全加固（XSS / CSRF / SQL 注入防御 / 接口签名）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td rowspan="3"><b>⚙️ 分布式系统</b></td>
      <td>ZooKeeper（选举机制 / 分布式协调 / 配置中心 / 分布式锁）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>分布式理论（CAP / BASE / Paxos / Raft）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>分布式事务（2PC / TCC / Saga / 消息最终一致性）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td rowspan="4"><b>🏗️ 架构设计</b></td>
      <td>三高架构（高性能 / 高可用 / 高扩展）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>DDD 领域驱动设计（限界上下文 / 聚合根 / 领域事件）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>业务架构 / Event Storming / 服务划分原则</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>架构模式（CQRS / Event Sourcing / Saga / Outbox Pattern）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td rowspan="3"><b>🎯 系统设计与面试题</b></td>
      <td>系统设计方法论 / 容量估算 / 核心组件选型</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>真实场景设计题（短链 / 秒杀 / 消息推送 / Feed 流 / 搜索）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>大厂高频面试题（美团 / 阿里 / 字节 / 腾讯）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td rowspan="4"><b>🛡️ 稳定性保障</b></td>
      <td>限流（令牌桶 / 漏桶算法 / Sentinel / Redis 限流）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>熔断降级（Hystrix / Resilience4j）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>幂等性设计（Token / 数据库唯一键 / Redis 去重）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>冗余与高可用（多副本 / 异地多活）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td rowspan="3"><b>🐳 容器与云原生</b></td>
      <td>Docker（镜像构建 / 网络模型 / Volume 管理）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>Kubernetes（Pod / Service / Ingress / HPA / 滚动发布）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>Crane（美团内部容器调度平台实践）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td rowspan="3"><b>🔧 构建与工程化</b></td>
      <td>Git（分支策略 / Rebase vs Merge / Hooks）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>Gradle（多模块构建 / 自定义 Task / 增量构建）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>Maven（生命周期 / 插件机制 / 私服管理）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td rowspan="8"><b>🐘 大数据生态</b></td>
      <td>Hadoop（HDFS 架构 / MapReduce / YARN 调度）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>Hive（HQL / 分区分桶 / ORC/Parquet / Tez/Spark 引擎）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>Spark（RDD / DataFrame / SparkSQL / Streaming / 调优）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>Flink（流批一体 / 事件时间与窗口 / 状态管理 / Checkpoint）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>Presto / Trino（联邦查询 / OLAP 即席分析）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>数据湖（Delta Lake / Apache Iceberg / Hudi 对比选型）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>数据仓库（ODS/DWD/DWS/ADS 分层 / 星形/雪花建模）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>数据治理（元数据 / 血缘 / 数据质量 / Apache Atlas）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td rowspan="6"><b>📊 数据分析</b></td>
      <td>指标体系设计（北极星指标 / OKR / 指标拆解）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>埋点设计与数据采集（前后端埋点 / 数据质量治理）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>用户路径 / 留存 / 分群分析（漏斗 / Cohort / RFM）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>A/B 实验（设计 / 分流策略 / 显著性检验 / Holdout 组）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>归因分析 / 预测分析 / 增长分析（AARRR / HEART）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>分析工具（SQL 窗口函数 / Pandas / 可视化看板）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td rowspan="3"><b>🕷️ 爬虫、逆向与反爬</b></td>
      <td>爬虫基础 / 分布式爬虫 / JS 渲染页爬取</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>抓包分析 / JS 逆向 / App 逆向（jadx / SSL Pinning）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>反爬系统设计（设备指纹 / 行为识别 / 多层防护）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td rowspan="4"><b>🔰 风控系统</b></td>
      <td>业务风控（账号 / 交易 / 内容 / 活动风控）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>规则引擎（Drools）/ 设备指纹 / 图谱风控</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>AI 风控模型（特征工程 / 实时推理）/ 实时风控架构</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>风控系统设计（名单 / 事件总线 / 案例系统 / 度量）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td rowspan="6"><b>🌍 多语言拓展</b></td>
      <td>Go（Goroutine &amp; Channel / Gin / Gorm）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>Python（FastAPI / 数据处理 / 脚本自动化）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>Node.js（事件循环 / NestJS / BFF 层设计）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>Shell（Bash 语法 / 正则 / 自动化脚本）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>C / C++（指针与内存 / 编译链接 / 系统调用）</td>
      <td>🔜 待开始</td>
      <td>了解为主</td>
    </tr>
    <tr>
      <td>汇编语言（x86/ARM 指令集 / 栈帧结构）</td>
      <td>🔜 待开始</td>
      <td>了解为主</td>
    </tr>
    <tr>
      <td rowspan="3"><b>🖥️ 前端技术</b></td>
      <td>HTML5 / CSS3 / JavaScript（ES6+）/ TypeScript</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>React / Vue3 核心原理与工程实践</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>工程化（Webpack / Vite / 前后端联调 / API 设计）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td rowspan="4"><b>🧠 AI 算法理论</b></td>
      <td>机器学习基础（监督 / 无监督 / 强化学习 / 特征工程）</td>
      <td>🔜 待开始</td>
      <td>了解为主</td>
    </tr>
    <tr>
      <td>神经网络 / 深度学习（CNN / RNN / LSTM / Transformer）</td>
      <td>🔜 待开始</td>
      <td>了解为主</td>
    </tr>
    <tr>
      <td>大模型原理（Pre-training / SFT / RLHF / Scaling Law / MoE）</td>
      <td>🔜 待开始</td>
      <td>了解为主</td>
    </tr>
    <tr>
      <td>AI 框架（PyTorch / TensorFlow / HuggingFace Transformers）</td>
      <td>🔜 待开始</td>
      <td>了解为主</td>
    </tr>
    <tr>
      <td rowspan="4"><b>🤖 AI 与 Agent 应用开发</b></td>
      <td>大模型应用（Prompt 工程 / RAG 检索增强生成 / Fine-tuning）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>Agent 框架（LangChain / LangGraph / AutoGen / ReAct 模式）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>AI 工程化（向量数据库 / 模型部署 / 推理优化）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>Java AI 集成（Spring AI / 模型调用封装 / Function Calling）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
  </tbody>
</table>

---

## 🔗 关联项目

| 项目 | 定位 | 内容 |
|------|------|------|
| [`java_study`](../java_study) | 基础理论 | Java 语言核心、数据结构与算法、JVM、操作系统、计算机网络 |
| **本项目**（`java_fullstack_ai_agent_study`） | 工程实践 | Spring 生态、分布式架构、大数据生态、存储中间件、多语言、前端、AI/Agent 工程化 |
| [`ai_coding_harness_engineering_study`](../ai_coding_harness_engineering_study) | AI 工程 | AI 编程、Harness 工程理论、AI Coding 工具链、大模型应用及 Agent 开发知识沉淀 |

---

## 📅 更新记录

| 日期 | 版本 | 内容 |
|------|------|------|
| 2026-05-23 | v0.1.0 | 项目初始化，创建 README 与 .gitignore |
| 2026-05-23 | v0.2.0 | 补充大数据生态（Hadoop/Hive/Spark/Flink/数据湖/数仓/治理）|
| 2026-05-23 | v0.3.0 | 补充多语言拓展（Shell/C/C++/汇编）、AI 算法理论、关联第三个项目 |
| 2026-05-23 | v0.4.0 | 补充架构设计（三高/DDD/业务架构）、真实场景面试题、更新记录 |
| 2026-05-23 | v0.5.0 | 补充爬虫、逆向工程、反爬系统设计方向 |
| 2026-05-23 | v0.6.0 | 补充风控系统（业务风控/规则引擎/图谱风控/实时架构）|
| 2026-05-23 | v0.7.0 | 补充数据分析（指标/埋点/A/B实验/分析方法/工具）|
| 2026-05-23 | v0.8.0 | 重构项目定位说明、关联项目分工表、学习进度（按主子模块层级展示）|
| 2026-05-23 | v0.9.0 | 更新项目标题；学习进度改为带 rowspan 合并单元格的单张 HTML 大表格 |

---

<div align="center">
  <sub>持续更新中 🚀 · 学以致用，从实践中成长</sub>
</div>

