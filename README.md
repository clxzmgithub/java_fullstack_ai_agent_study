# 📚 Java 后端 & 全栈 & AI 应用接入 工程实践项目

<div align="center">

![Status](https://img.shields.io/badge/状态-持续更新中-brightgreen)
![License](https://img.shields.io/badge/license-MIT-blue)
![Java](https://img.shields.io/badge/Java-17%2B-orange)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.x-green)

</div>

---

## 📌 项目定位

本项目是一个面向**工程实践**的系统性学习仓库，**不是真实的生产项目**。聚焦于 Java 全栈工程化体系的深度实践，横跨后端架构、分布式系统、大数据生态、数据分析、风控与爬虫、前端、多语言拓展、AI/Agent **系统接入与工程落地**等方向，以动手实验、场景设计、面试题解析为主要学习载体，逐步构建完整的全栈工程师知识体系。

**核心学习方向（20 大板块）：**
`Spring 全家桶` · `数据库与存储` · `消息队列` · `分布式系统` · `架构设计` · `系统设计与面试题` · `稳定性保障` · `网络与通信` · `认证授权与安全` · `云计算 & 云原生` · `大数据生态` · `数据分析` · `爬虫·逆向·反爬·风控` · `多语言拓展 + 前端` · `AI/Agent 应用接入（做系统）` · `构建与工程化` · `业务架构与产品思维` · **`测试工程`**

> ⚠️ **关联项目分工说明**
>
> 本人维护三个相互补充、各有侧重的学习仓库，共同构成完整的知识体系：
>
> | 项目 | 定位 | 核心聚焦 |
> |------|:----:|---------|
> | [`java_study`](../java_study) | 🔵 基础理论 | Java 语言核心、并发深度、JVM 原理、IO/NIO 体系、数据结构与算法、设计模式、计算机基础理论、信息安全基础、软件工程基础、性能工程、调试排查、前沿技术趋势——**打地基** |
> | **本项目**（`java_fullstack_ai_agent_study`） | 🟠 工程实践 | Spring 生态、分布式架构、大数据、存储中间件、风控爬虫、数据分析、多语言、AI/Agent 系统接入、测试工程——**做系统** |
> | [`ai_coding_harness_engineering_study`](../ai_coding_harness_engineering_study) | 🟣 AI 工程 | AI 编程方法论、上下文工程、AI 工具工程化、Harness 理论、AI Coding 工具链、大模型与 Agent 开发知识——**用 AI 提效** |

> 📐 **AI/Agent 在两个项目中的分工边界**
>
> | 关注点 | 本项目（做系统）| `ai_coding_harness_engineering_study`（用 AI 提效）|
> |--------|:-------------:|:-----------------------------------------------:|
> | Spring AI 接入、模型 API 调用 | ✅ | — |
> | RAG 系统工程化（向量数据库集成/检索服务）| ✅ | — |
> | Function Calling 封装与业务对接 | ✅ | — |
> | 模型调用稳定性（超时/熔断/限流/成本）| ✅ | — |
> | AI 算法原理（Transformer/RLHF/MoE）| — | ✅ |
> | Agent 编排框架（LangGraph/AutoGen/CrewAI）| — | ✅ |
> | Agent SDK 对比与设计哲学 | — | ✅ |
> | MCP 协议原理与扩展开发 | — | ✅ |
> | Harness/Eval 框架（LLM-as-Judge）| — | ✅ |
> | AI Coding 工具使用（Claude Code/Cursor）| — | ✅ |

---

## 🗺️ 技术版图

> 💡 **如何使用这张地图**：先看「学习路线总览」找到你当前所在位置和下一步，再进入对应章节查看详细学习要点，最后在「学习进度」表里打卡。三张表联动，不会迷路。

### 📍 学习路线总览

> 优先级说明：🔴 核心必学 ｜ 🟠 重要补充 ｜ 🟡 按需拓展 ｜ 🔵 了解即可

| # | 板块 | 优先级 | 前置依赖 | 学习目标 | 美团内部对应 |
|:-:|------|:------:|---------|---------|------------|
| 1 | 🧩 **Spring 全家桶** | 🔴 核心 | Java 基础（见 `java_study`）| 能独立搭建 Spring Boot 工程，理解 IoC/AOP/事务/MVC 源码级原理，会用 Spring Cloud 搭建微服务 | MDP / XFrame 开发框架 |
| 2 | 🗄️ **数据库与存储** | 🔴 核心 | Spring 全家桶 | 能做 MySQL 索引优化与分库分表方案，熟练使用 Redis 缓存体系，会 ES 全文检索集成 | RDS / Zebra / Squirrel / Cellar / S3Plus |
| 3 | 📨 **消息队列** | 🔴 核心 | Spring 全家桶 | 理解 Kafka 分区设计与幂等事务消息，能处理消息积压，会设计异步解耦方案 | Mafka |
| 4 | ⚙️ **分布式系统** | 🔴 核心 | 数据库 + 消息队列 | 理解 CAP/Raft/Paxos 理论，能选型并实现分布式事务（TCC/Saga），掌握分布式锁方案 | OCTO / Cerberus / Lion |
| 5 | 🛡️ **稳定性保障** | 🔴 核心 | 分布式系统 | 能设计限流/熔断/降级方案，掌握幂等性保障手段，理解多副本与异地多活 | Sentinel / Resilience4j |
| 6 | 🌐 **网络与通信** | 🟠 重要 | Java 基础 | 理解 NIO 原理和 Netty 架构，能自定义 RPC 协议，掌握 gRPC/Thrift 使用 | Pigeon / OCTO / Shark |
| 7 | 🔐 **认证授权与安全** | 🟠 重要 | Spring 全家桶 | 能独立实现 JWT/OAuth2/SSO 登录体系，掌握 RBAC 权限模型，熟悉常见安全攻防 | SSO / ePassport |
| 8 | 🏗️ **架构设计** | 🟠 重要 | Spring + 分布式 | 能做系统容量估算，会用 DDD 进行领域划分，能设计三高（高性能/高可用/高扩展）架构 | 内部架构评审体系 |
| 9 | ☁️ **云计算 & 云原生** | 🟠 重要 | 架构设计 | 熟悉 Docker/K8s 核心概念，能配置 CI/CD 流水线，理解可观测性体系（监控/日志/链路） | HULK / Crane / MCD / Raptor |
| 10 | 🎯 **系统设计与面试题** | 🟠 重要 | 1~9 板块综合 | 能独立设计短链/秒杀/Feed 流/推送等经典系统，应对大厂后端面试 | — |
| 11 | 🔧 **构建与工程化** | 🟡 按需 | 无 | 熟练使用 Git 工作流，能用 Gradle/Maven 管理多模块工程 | Plus（发布系统）|
| 12 | 🐘 **大数据生态** | 🟡 按需 | 数据库基础 | 理解 Hadoop/Hive/Spark/Flink 架构与使用场景，能设计分层数仓，掌握数据治理方法 | WanXiang / Spark / Flink / Hive |
| 13 | 📊 **数据分析** | 🟡 按需 | 大数据生态 | 能设计指标体系与埋点规范，会做 A/B 实验，熟悉 AARRR 增长分析框架 | MDBI（魔数）/ Ocean / Analytics |
| 14 | 💼 **业务架构与产品思维** | 🟡 按需 | 架构设计 | 能用 Event Storming 划分服务边界，理解电商/O2O 业务模型，能从技术视角评估商业可行性 | 各业务公共服务（POI/用户/支付）|
| 15 | 🕷️ **爬虫、逆向与反爬** | 🟡 按需 | Python / 网络基础 | 能独立开发分布式爬虫，掌握 JS/App 逆向基础，能设计多层反爬系统 | 安全类工具导航 |
| 16 | 🔰 **风控系统** | 🟡 按需 | 分布式 + 大数据 | 能设计实时风控架构（规则+模型融合），理解设备指纹与图谱风控，掌握风控度量体系 | 安全类工具导航 |
| 17 | 🤖 **AI/Agent 应用接入** | 🟠 重要 | Spring + 数据库 | 能用 Spring AI 构建可运行的 RAG 应用，封装 Function Calling 业务接口，能解决生产级稳定性问题（超时/熔断/成本控制）| MLP / Turing / Horus |
| 18 | 🌍 **多语言拓展** | 🔵 了解 | 各语言入门 | Go/Python/Node.js 达到可做实际项目水平，Shell 能写自动化脚本，C/汇编了解即可 | — |
| 19 | 🖥️ **前端技术** | 🔵 了解 | JavaScript 基础 | 能独立实现 React/Vue3 业务页面，理解前后端联调与 API 设计，具备全栈开发能力 | 前端类工具导航 |
| 20 | 🧪 **测试工程** | 🟡 按需 | Spring 全家桶 + 分布式 | 能编写高质量单元/集成测试，掌握压力测试和性能测试方法论，建立完整的测试分层体系 | 测试平台（研发运维工具）|

> 📌 **推荐学习主线**（适合后端工程师）：`1 Spring` → `2 数据库` → `3 消息队列` → `4 分布式` → `5 稳定性` → `8 架构设计` → `10 系统设计面试` → 根据方向选择其余板块

---

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

#### 🔬 重点源码学习
| 源码模块 | 核心类 / 方法 | 学习要点 |
|----------|--------------|----------|
| **IoC 容器启动** | `AbstractApplicationContext#refresh()` | 12 步启动流程 / BeanDefinition 注册 / BeanFactory 初始化 |
| **Bean 生命周期** | `AbstractAutowireCapableBeanFactory#doCreateBean()` | 实例化 → 属性注入 → Aware → BeanPostProcessor → init → 销毁 |
| **AOP 代理创建** | `AbstractAutoProxyCreator#postProcessAfterInitialization()` | JDK 动态代理 vs CGLIB / 切点匹配 / 拦截器链执行 |
| **事务管理** | `TransactionInterceptor#invoke()` | 事务传播行为 / 开启-提交-回滚流程 / 与 AOP 的结合 |
| **自动装配** | `AutoConfigurationImportSelector#selectImports()` | `spring.factories` / 条件装配 `@Conditional` / SPI 机制 |
| **MVC 请求处理** | `DispatcherServlet#doDispatch()` | HandlerMapping → HandlerAdapter → 参数解析 → 返回值处理 |
| **事件机制** | `SimpleApplicationEventMulticaster#multicastEvent()` | 同步/异步事件 / 观察者模式 / 自定义事件 |
| **循环依赖** | 三级缓存（`singletonObjects` / `earlySingletonObjects` / `singletonFactories`）| 解决流程 / 为何二级缓存不够 / 构造注入为何无法解决 |
| **Spring Cloud Gateway** | `RoutePredicateHandlerMapping` / `FilteringWebHandler` | 路由匹配 / 过滤器链 / 全局过滤器 vs 局部过滤器 |
| **OpenFeign 调用链** | `FeignClientFactoryBean` / `ReflectiveFeign#newInstance()` | 动态代理生成 / 负载均衡集成 / 重试与降级 |

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
- **常见架构模式**：CQRS / Event Sourcing / Saga / Outbox Pattern / Strangler Fig

### 💼 业务架构与产品思维

> 💡 AI 时代的全栈开发者不仅需要运用技术解决问题，更需能看懂业务、理解产品、主动提出方案。技术与业务的语言转换能力是引领力的核心。

| 方向 | 学习要点 |
|------|----------|
| **业务建模与领域划分** | 领域识别（用户域 / 订单域 / 支付域 / 品类域）/ 限界上下文 / 上下文戏图（Context Map）|
| **事件风暴（Event Storming）** | 用事件串联业务流程 / 识别聚合根与划分服务边界 |
| **微服务 vs 单体权衡** | 服务拆分时机 / 单体优先 / 勿过度设计 / 渐进式拆分策略 |
| **业务指标体系** | GMV / DAU / 转化漏斗 / 留存率 / 商业可行性分析 |
| **需求分析与方案设计** | 业务需求拆解（用户故事 / PRD 解读）/ 技术方案评估与指引 |
| **行业认知与业务职能** | 电商 / O2O / 内容社区 / SaaS / 到家外卖平台业务理解 |
| **产品思维** | 用户分层与画像 / 需求的显性与隐性 / MVP 思维 / 项目型 vs 产品型思维转变 |
| **AI 赋能业务** | AI 改造传统业务流程 / 智能化产品设计方法论 / Copilot 、智能客服、个性化应用场景 |

### 🛡️ 稳定性保障
| 方向 | 技术与方案 |
|------|-----------|
| 限流 | 令牌桶 / 漏桶算法 / Sentinel / Redis 限流 |
| 熔断降级 | Hystrix / Resilience4j / 服务降级策略 |
| 幂等性 | Token 机制 / 数据库唯一键 / Redis 去重 |
| 冗余 | 数据冗余 / 服务多副本 / 异地多活 |

### ☁️ 云计算 & 云原生

| 方向 | 技术与方案 |
|------|----------|
| **容器化** | Docker（镜像构建 / 多阶段构建 / 网络模型 / Volume 管理）|
| **容器编排** | Kubernetes（Pod / Deployment / Service / Ingress / HPA / 滚动发布 / 灰度）|
| **Service Mesh** | Istio / Envoy（流量管理 / 熔断 / 链路追踪 / mTLS）|
| **Serverless** | FaaS 原理 / 冷启动优化 / 云函数应用场景 |
| **云平台核心服务** | 计算（ECS/EKS）/ 存储（OSS/S3）/ 网络（VPC/LB/NAT）/ 数据库云服务 |
| **IaC 基础设施即代码** | Terraform / Helm Chart / ArgoCD / GitOps 工作流 |
| **可观测性** | Prometheus + Grafana / ELK / Jaeger 链路追踪 / OpenTelemetry |
| **CI/CD** | Jenkins / GitHub Actions / 流水线设计 / 蓝绿/金丝雀发布 |
| **内部平台实践** | Crane（美团容器调度）/ HULK（美团云平台）/ 云原生改造落地 |

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

### 🤖 AI/Agent 应用接入（做系统）

> 💡 **本章聚焦「做系统」**——目标是交付可运行的 AI 业务代码。算法原理、Agent SDK 对比、AI 工具使用方法论等内容见 [`ai_coding_harness_engineering_study`](../ai_coding_harness_engineering_study)。

#### 🔌 大模型 API 接入与封装
| 方向 | 学习要点 |
|------|---------|
| Spring AI 框架 | ChatClient / ChatModel / Advisors / EmbeddingModel / ImageModel |
| 模型 API 对接 | OpenAI / Anthropic Claude / 国内模型（DeepSeek / 通义 / 文心）接入 |
| Prompt 管理 | PromptTemplate / SystemMessage / 多轮对话构建 |
| 流式响应处理 | Streaming API / SSE 推送 / 前端实时渲染集成 |
| 多模型路由 | 模型能力分级 / 按场景路由 / 降级备用模型策略 |

#### 📚 RAG 系统工程化
| 方向 | 学习要点 |
|------|---------|
| 向量数据库集成 | Milvus / Chroma / PgVector / Redis Vector 接入与 Spring AI 集成 |
| 文档处理管线 | 文档解析（PDF/Word/HTML）/ Chunking 策略 / Embedding 批处理 |
| 检索服务构建 | 向量检索 / 关键词检索 / 混合检索接口封装 |
| RAG 应用实战 | 企业知识库问答 / 文档智能搜索 / 代码库检索 |
| 数据更新策略 | 增量索引 / 版本管理 / 文档失效处理 |

#### ⚙️ Function Calling 与 Agent 工具封装
| 方向 | 学习要点 |
|------|---------|
| Function Calling 原理 | 工具定义规范（JSON Schema）/ 工具调用循环机制 |
| Spring AI Function | `@Bean` 注册工具 / FunctionCallback 接口 / 自动发现机制 |
| 业务工具封装 | 数据库查询工具 / HTTP 外部 API 工具 / 内部微服务工具 |
| 工具调用安全 | 参数校验 / 权限控制 / 调用结果脱敏 |
| MCP 服务端开发 | 用 Java/Spring 实现 MCP Server，暴露内部能力给 AI 工具 |

#### 🛡️ 生产级稳定性保障
| 方向 | 学习要点 |
|------|---------|
| 超时与熔断 | 模型调用超时设置 / Resilience4j 熔断 / 快速失败策略 |
| 重试策略 | 指数退避重试 / 幂等重试设计 / 最大重试次数控制 |
| 成本控制 | Token 用量统计 / 请求限频（Rate Limit）/ 缓存重复请求 |
| 异步化处理 | 长时推理异步化 / 任务队列（Kafka/MQ）/ 结果回调通知 |
| 可观测性 | 模型调用链路追踪 / Token 用量监控看板 / 异常率告警 |

---

## 📁 项目结构

> 🚧 目录结构规划中，随学习进度逐步创建与完善。

### 🏢 美团工具服务导航 — 理论到生产的映射

> 📌 **这部分是什么？** 上面 19 个板块学的都是"通用技术"，而 `美团工具服务导航/` 目录记录的是**这些技术在美团生产环境中的具体落地形态**。每学完一个技术板块，可以对照下表找到美团对应的内部系统，加深理解"真实系统是怎么做的"。

| 通用技术 | 美团内部对应工具 | 所在文件 |
|---------|---------------|---------|
| Spring Boot / 微服务框架 | MDP、XFrame | 研发运维工具.md |
| 服务注册发现 / 治理 | OCTO、Lion（配置）| 研发运维工具.md / 架构类.md |
| 发布 / CI/CD | Plus、MCD | 研发运维工具.md |
| 监控告警 / 可观测性 | Raptor、LogCenter | 研发运维工具.md |
| MySQL 托管 / 分库分表 | RDS、Zebra、Blade | 架构类.md |
| Redis / KV 缓存 | Squirrel（内存）、Cellar（持久）| 架构类.md |
| 对象存储 | S3Plus、Venus（图片）| 架构类.md |
| Kafka / 消息队列 | Mafka、Pike（移动端）| 架构类.md |
| 定时任务调度 | Crane | 架构类.md |
| 分布式锁 | Cerberus | 架构类.md |
| API 网关 | Shepherd、Oceanus（七层）、MGW（四层）| 架构类.md |
| Hadoop / Spark / Flink | WanXiang、Spark 内存批处理、RT 实时计算 | 数据类.md |
| OLAP 即席查询 | Presto Adhoc、Talos | 数据类.md |
| BI / 数据分析平台 | MDBI（魔数）| 数据类.md |
| 机器学习平台 | MLP、Turing、MLX | 数据类.md |
| 用户行为采集 | Analytics（灵犀）、Ocean | 数据类.md |
| JWT / SSO / 认证授权 | SSO、MTUserCenter、ePassport | 安全类.md / 业务公共服务.md |
| 风控 / 安全防护 | 各安全工具 | 安全类.md |
| 前端框架 / 低代码 | Picasso、Mach、Rhino | 前端类.md |
| IM / 消息推送 / SMS | IM 即时通讯、Hedwig、SMS、TTS | 通讯类.md |
| 设计协作 / UI 规范 | Ingee（印迹）、Cookie（曲奇）| 设计类.md |
| 用户中心 / 地图 / 支付 | MTUserCenter、MAF、PayCashier | 业务公共服务.md |
| 大模型 / AI 服务 | MLP（模型平台）、Horus（AI 中台）、Turing | 数据类.md |

```
java_fullstack_ai_agent_study/
├── README.md                    # 项目总览（当前文件）
├── meituan_work_space(MWS).md   # 美团内部技术平台组件索引（MWS）
│
├── 美团工具服务导航/              # 美团内部工具服务导航
│   ├── 工程师工具导航/           #   按岗位角色划分的工具导航
│   │   ├── 前端工程师.md         #     前端工程师工具导航
│   │   ├── 后台&系统工程师.md    #     后台 & 系统工程师工具导航
│   │   ├── 算法工程师.md         #     算法工程师工具导航
│   │   ├── 数据工程师.md         #     数据工程师工具导航
│   │   ├── 测试工程师.md         #     测试工程师工具导航
│   │   └── 运维工程师.md         #     运维工程师工具导航
│   └── 公共服务工具导航/         #   按类别划分的公共工具全览
│       ├── 研发运维工具.md       #     发布 / 监控 / 测试 / 开发 / 协作工具
│       ├── 前端类.md             #     前端框架 / 跨端 / 低代码 / 可视化工具
│       ├── 安全类.md             #     风控 / 网络安全 / 合规工具
│       ├── 数据类.md             #     大数据 / BI / 机器学习 / 用户行为工具
│       ├── 架构类.md             #     服务治理 / 消息队列 / 网关 / 存储 / 容器
│       ├── 设计类.md             #     设计协作 / 物料生产 / UI 一致性工具
│       ├── 通讯类.md             #     IM / 短信 / Push / 语音通话工具
│       └── 业务公共服务.md       #     用户账号 / 地图 / 支付 / POI / 运营工具
│
├── spring/                      # Spring 全家桶实践
│   ├── spring-core/             #   IoC / AOP 实验
│   ├── spring-boot/             #   自动装配 / Starter 开发
│   ├── spring-cloud/            #   微服务体系
│   ├── spring-security/         #   认证授权
│   └── source-code/             #   重点源码分析（IoC/AOP/事务/MVC/自动装配）
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
│   └── arch-patterns/           #   CQRS / Event Sourcing / Saga 等
│
├── business-arch/               # 业务架构与产品思维
│   ├── domain-modeling/         #   领域建模 / 边界划分
│   ├── event-storming/          #   事件风暴实践
│   ├── industry-knowledge/      #   行业认知（电商/O2O/SaaS/到家等）
│   ├── metrics/                 #   业务指标体系
│   └── ai-product/              #   AI 赋能业务应用设计
│
├── system-design/               # 系统设计案例
│   ├── scenarios/               #   真实场景设计题（短链/秒杀/Feed流等）
│   └── interview-questions/     #   大厂高频面试题整理
│
├── high-performance/            # 高性能 / 高可用
│
├── stability/                   # 稳定性（限流 / 熔断 / 幂等）
│
├── cloud-native/                # 云计算 & 云原生
│   ├── docker/                  #   容器化基础
│   ├── kubernetes/              #   K8s 核心与实践
│   ├── service-mesh/            #   Istio / Envoy
│   ├── observability/           #   可观测性（Prometheus/Grafana/Jaeger）
│   ├── cicd/                    #   CI/CD 流水线
│   ├── iac/                     #   基础设施即代码（Terraform/Helm/ArgoCD）
│   └── cloud-platform/          #   云平台核心服务与内部平台实践
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
├── ai-agent/                    # AI/Agent 应用接入（做系统）
│   ├── spring-ai/               #   Spring AI 框架实践（ChatClient / Advisors）
│   ├── rag/                     #   RAG 系统工程化（向量库集成 / 检索管线）
│   ├── function-calling/        #   Function Calling 封装（Spring AI Function）
│   ├── mcp-server/              #   Java/Spring 实现 MCP Server（对外暴露能力）
│   └── stability/               #   生产级稳定性（超时/熔断/成本控制/可观测性）
│
└── testing/                     # 🧪 测试工程
    ├── unit-testing/            #   单元测试（JUnit 5 + Mockito）
    │   ├── junit5/              #     JUnit 5 注解体系 / 断言 API / 参数化测试
    │   └── mockito/             #     Mock / Stub / Spy / ArgumentCaptor
    ├── integration-testing/     #   集成测试
    │   ├── spring-boot-test/    #     @SpringBootTest / @DataJpaTest / @WebMvcTest
    │   ├── testcontainers/      #     Testcontainers（MySQL/Redis/Kafka 真实环境）
    │   └── wiremock/            #     WireMock HTTP 服务 Mock
    ├── performance-testing/     #   性能测试 / 压力测试
    │   ├── jmh/                 #     JMH 微基准测试（@Benchmark / 预热 / 测量陷阱）
    │   ├── jmeter/              #     JMeter（线程组 / 分布式压测 / 测试计划设计）
    │   ├── gatling/             #     Gatling（Scala DSL / 场景建模 / 压测报告）
    │   └── k6/                  #     K6（JS 脚本压测 / 灵活场景 / 指标导出）
    ├── api-testing/             #   API 测试（REST Assured / MockMvc）
    ├── contract-testing/        #   契约测试（Spring Cloud Contract / Pact）
    ├── chaos-engineering/       #   混沌工程（Chaos Monkey / 故障注入）
    └── test-design/             #   测试用例设计（等价类 / 边界值 / TDD / BDD）
```

---

### 🧪 测试工程

> 💡 **工程质量的最后一道防线**。从单元测试到压力测试，建立分层测试体系，是全栈工程师不可缺失的硬技能。AI 时代更需要可靠的测试作为 AI 生成代码的验证基础（Harness）。

#### 🏗️ 测试分层体系
| 层次 | 方向 | 学习要点 |
|------|------|---------|
| **单元测试** | JUnit 5 | 注解体系（`@Test` / `@ParameterizedTest` / `@BeforeEach`）/ 断言 API / 测试生命周期 |
| **单元测试** | Mockito | `@Mock` / `@InjectMocks` / `when-thenReturn` / `verify` / `ArgumentCaptor` / Spy |
| **集成测试** | Spring Boot Test | `@SpringBootTest` / `@DataJpaTest` / `@WebMvcTest` / `@MockBean` / TestRestTemplate |
| **集成测试** | Testcontainers | Docker 容器化集成测试 / MySQL/Redis/Kafka 真实环境测试 / 与 JUnit 5 集成 |
| **契约测试** | Spring Cloud Contract / Pact | 服务间接口契约验证 / 消费者驱动契约测试 |
| **端到端测试** | Selenium / Playwright | 浏览器自动化 / 测试场景编写 / CI 集成 |

#### 📐 测试用例设计方法论
| 方法 | 学习要点 |
|------|---------|
| 等价类划分 | 有效等价类 / 无效等价类 / 边界值选取策略 |
| 边界值分析 | 最小值 / 最大值 / 边界 ±1 / 特殊值（null/0/空字符串）|
| 因果图 / 判定表 | 多条件组合 / 简化判定表方法 |
| 场景测试法 | 主成功场景 / 扩展场景 / 异常场景 / 备选路径 |
| TDD（测试驱动开发）| 红-绿-重构循环 / 测试先行 / 设计反馈 |
| BDD（行为驱动开发）| Given-When-Then 格式 / Cucumber / 与业务语言对齐 |
| 测试覆盖率 | 行覆盖 / 分支覆盖 / 条件覆盖 / JaCoCo 工具使用 |

#### 🔥 性能测试
| 方向 | 学习要点 |
|------|---------|
| 性能测试方法论 | 性能测试类型（基准/负载/压力/稳定性/尖峰测试）/ 性能指标（TPS/QPS/响应时间/并发数/错误率）|
| JMH 微基准测试 | `@Benchmark` / 基准测试模式 / JVM 预热（Warmup）/ 避免死码消除 / 测量陷阱 |
| JMeter | 测试计划设计 / 线程组 / 采样器 / 监听器 / 分布式压测 / 参数化 |
| Gatling | 基于 Scala DSL 的高并发压测 / 场景建模 / 断言与报告 / 与 CI/CD 集成 |
| K6 | JavaScript 脚本压测 / 灵活场景编排 / 指标导出 / 云端压测 |
| 压测结果分析 | 性能瓶颈定位（CPU/内存/IO/锁）/ 火焰图辅助分析 / 与监控告警结合 |

#### 🔌 集成测试进阶
| 方向 | 学习要点 |
|------|---------|
| Testcontainers 实战 | 数据库（MySQL/PostgreSQL）/ 缓存（Redis）/ 消息队列（Kafka）/ 使用 `@Container` + `@DynamicPropertySource` |
| WireMock | HTTP 依赖服务 Mock / Stub 录制回放 / 请求匹配策略 / 与 Spring 集成 |
| 测试数据管理 | `@Sql` 脚本 / `@Transactional` 测试回滚 / TestDataBuilder 模式 / Fixture 工厂 |
| API 测试 | REST Assured / `MockMvc` 链式 API / 接口自动化测试 |
| 混沌工程 | Chaos Engineering 理念 / Chaos Monkey / 故障注入（网络延迟/节点宕机）/ 稳定性验证 |

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
      <td rowspan="6"><b>🧩 Spring 全家桶</b></td>
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
      <td>🔬 重点源码（IoC 启动 / Bean 生命周期 / AOP 代理 / 事务 / 自动装配 / MVC / 循环依赖）</td>
      <td>🔜 待开始</td>
      <td>深度优先</td>
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
      <td rowspan="3"><b>🏗️ 架构设计</b></td>
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
      <td>架构模式（CQRS / Event Sourcing / Saga / Outbox Pattern）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td rowspan="8"><b>💼 业务架构与产品思维</b></td>
      <td>领域建模与划分（用户域 / 订单域 / 支付域 / Context Map）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>事件风暴（Event Storming）— 用事件识别业务流程与服务边界</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>微服务 vs 单体权衡（拆分时机 / 单体优先 / 渐进式拆分）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>业务指标体系（GMV / DAU / 漏斗转化 / 商业可行性分析）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>需求分析与方案评估（PRD 解读 / 用户故事 / 技术方案对比）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>行业认知（电商 / O2O / 内容社区 / SaaS / 到家外卖平台业务理解）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>产品思维（用户分层 / 显性与隐性需求 / MVP / 项目型 vs 产品型思维）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>AI 赋能业务（智能化改造流程 / Copilot / 智能客服 / 个性化推荐应用）</td>
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
      <td rowspan="9"><b>☁️ 云计算 & 云原生</b></td>
      <td>Docker（镜像构建 / 多阶段构建 / 网络模型 / Volume 管理）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>Kubernetes（Pod / Deployment / Service / Ingress / HPA / 滚动发布）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>Service Mesh — Istio / Envoy（流量管理 / 熔断 / mTLS / 链路追踪）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>Serverless — FaaS 原理 / 冷启动优化 / 云函数应用场景</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>云平台核心服务（计算 / 对象存储 / VPC / 托管数据库）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>IaC 基础设施即代码（Terraform / Helm Chart / ArgoCD / GitOps）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>可观测性（Prometheus + Grafana / ELK / Jaeger / OpenTelemetry）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>CI/CD 流水线（Jenkins / GitHub Actions / 蓝绿 / 金丝雀发布）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>内部平台实践（Crane 容器调度 / HULK 云平台 / 云原生改造落地）</td>
      <td>🔜 待开始</td>
      <td>美团内部</td>
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
      <td rowspan="9"><b>🤖 AI/Agent 应用接入（做系统）</b></td>
      <td>Spring AI 框架（ChatClient / Advisors / EmbeddingModel）</td>
      <td>🔜 待开始</td>
      <td>🔑 重点</td>
    </tr>
    <tr>
      <td>模型 API 对接（OpenAI / Claude / DeepSeek / 通义）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>Prompt 管理与流式响应处理（SSE / 前端实时集成）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>RAG 系统工程化（向量库集成 / 文档管线 / 混合检索）</td>
      <td>🔜 待开始</td>
      <td>🔑 重点</td>
    </tr>
    <tr>
      <td>Function Calling 封装与业务工具对接（Spring AI Function）</td>
      <td>🔜 待开始</td>
      <td>🔑 重点</td>
    </tr>
    <tr>
      <td>MCP Server 开发（Java/Spring 对外暴露能力）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>生产级稳定性：超时 / 熔断 / 重试设计</td>
      <td>🔜 待开始</td>
      <td>🔑 重点</td>
    </tr>
    <tr>
      <td>成本控制：Token 统计 / Rate Limit / 缓存重复请求</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>可观测性：模型调用链路追踪 / Token 监控看板 / 告警</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td rowspan="9"><b>🧪 测试工程</b></td>
      <td>单元测试：JUnit 5（注解体系 / 参数化测试 / 断言 API）</td>
      <td>🔜 待开始</td>
      <td>🔑 重点</td>
    </tr>
    <tr>
      <td>单元测试：Mockito（Mock / Stub / Spy / ArgumentCaptor）</td>
      <td>🔜 待开始</td>
      <td>🔑 重点</td>
    </tr>
    <tr>
      <td>集成测试：Spring Boot Test（@SpringBootTest / @DataJpaTest / @WebMvcTest）</td>
      <td>🔜 待开始</td>
      <td>🔑 重点</td>
    </tr>
    <tr>
      <td>集成测试：Testcontainers（MySQL/Redis/Kafka 真实环境测试）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>API 测试：REST Assured / MockMvc 链式 API / 接口自动化</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>性能测试方法论（TPS/QPS/响应时间/并发数 / 测试类型分类）</td>
      <td>🔜 待开始</td>
      <td>🔑 重点</td>
    </tr>
    <tr>
      <td>JMeter / Gatling / K6 压力测试工具实战（分布式压测 / 报告分析）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>JMH 微基准测试（@Benchmark / 预热 / 避免死码消除）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
    <tr>
      <td>测试用例设计（等价类 / 边界值 / TDD / BDD / 测试覆盖率 JaCoCo）</td>
      <td>🔜 待开始</td>
      <td></td>
    </tr>
  </tbody>
</table>

---

## 🔗 关联项目

| 项目 | 定位 | 内容 |
|------|------|------|
| [`java_study`](../java_study) | 基础理论 | Java 语言核心（含 SPI/字节码增强/序列化）、JVM 原理、IO/NIO 体系、并发深度（含虚拟线程/响应式）、数据结构与算法、设计模式与设计原则、计算机基础理论（OS/网络/原理/编译）、信息安全基础（密码学/攻防）、软件工程基础（测试/重构/CI）、数学基础、性能工程（JMH/火焰图）、调试与问题排查（Arthas/JFR）、前沿技术趋势 |
| **本项目**（`java_fullstack_ai_agent_study`） | 工程实践 | Spring 生态、分布式架构、大数据生态、存储中间件、多语言、前端、AI/Agent 系统接入、测试工程（做系统）|
| [`ai_coding_harness_engineering_study`](../ai_coding_harness_engineering_study) | AI 工程 | AI 编程方法论、上下文工程、AI 工具工程化、Harness 理论、AI Coding 工具链、大模型与 Agent 知识——用 AI 提效 |

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
| 2026-05-24 | v1.0.0 | 新增「云计算 & 云原生」完整方向（容器/K8s/ServiceMesh/Serverless/可观测性/IaC/CI/CD）|
| 2026-05-24 | v1.1.0 | 新增「业务架构与产品思维」方向（领域建模/事件风暴/行业认知/产品思维/AI赋能业务）|
| 2026-05-24 | v1.2.0 | 新增「学习路线总览表」（20板块/优先级/前置依赖/学习目标/美团内部对应）；新增「开源技术→美团内部工具映射表」；完善「美团工具服务导航」定位说明 |
| 2026-06-10 | v1.3.0 | **项目定位重构**：明确「做系统」与「用 AI 提效」的边界，删除「🧠 AI 算法理论」章节（迁移至 `ai_coding_harness_engineering_study`）；将「🤖 AI 与 Agent 应用开发」重构为「🤖 AI/Agent 应用接入（做系统）」，聚焦 Spring AI 接入、RAG 工程化、Function Calling 封装、MCP Server 开发、生产稳定性保障；新增 AI/Agent 两项目分工边界对照表；更新学习路线总览表（19 大板块）、学习进度、项目结构、关联项目说明 |
| 2026-06-10 | v1.4.0 | **新增「🧪 测试工程」板块**：新增测试分层体系（JUnit 5 / Mockito / Spring Boot Test / Testcontainers / 契约测试 / E2E 测试）；新增测试用例设计方法论（等价类/边界值/TDD/BDD/覆盖率）；新增性能测试（JMH/JMeter/Gatling/K6/压测结果分析）；新增集成测试进阶（Testcontainers 实战/WireMock/测试数据管理/API 测试/混沌工程）；更新核心学习方向（19→20 大板块）、学习路线总览表、项目结构（`testing/` 目录）、学习进度表 |
| 2026-06-10 | v1.5.0 | **同步关联项目描述**：更新「关联项目分工说明」表和「关联项目」章节中 `java_study` 的描述，与其 README v1.3.0 保持一致（新增 IO/NIO 体系、信息安全、软件工程、性能工程、调试排查、前沿趋势等 14 大板块完整覆盖） |

---

<div align="center">
  <sub>持续更新中 🚀 · 学以致用，从实践中成长</sub>
</div>