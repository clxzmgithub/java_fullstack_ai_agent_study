# java_fullstack_ai_agent_study

> 📌 **项目定位说明**：本项目不是一个真实的生产工程项目，而是一个系统性的**全栈技术学习与实践工程**，聚焦于 Java 后端全栈、前端、AI/Agent 应用开发等工程技术的实践探索。
>
> 🔗 **与 `java_study` 项目的分工**：Java 语言核心 + 计算机基础理论（数据结构、算法、操作系统、网络协议等）已在 [`java_study`](../java_study) 项目中系统学习，本项目不再重复，专注于**工程实践与架构落地**。

---

## 🎯 学习目标

本项目覆盖以下技术方向的学习、实验与实践：

---

## 📚 技术版图

### 🧩 Spring 全家桶
- Spring Framework / Spring Boot / Spring MVC
- Spring Cloud（微服务体系：Nacos、Gateway、OpenFeign、Sleuth 等）
- Spring Security / Spring Data
- Spring Batch / Spring Integration

### 🗄️ 数据库与存储
- **MySQL**：SQL 优化、索引原理、事务与锁、主从复制、分库分表
- **Redis**：数据结构、持久化、集群、缓存策略、分布式锁
- **Elasticsearch**：全文检索、索引设计、聚合分析
- **MongoDB**：文档模型、适用场景、性能调优
- **HBase**：大宽表设计、RowKey 设计、与 Hadoop 生态集成

### 📨 消息队列
- **Kafka**：生产消费模型、分区设计、幂等性、事务消息、消息积压处理

### 🔧 构建与版本控制
- **Git**：工作流、分支策略、冲突解决、Hooks
- **Gradle**：多模块构建、依赖管理、自定义 Task
- **Maven**：生命周期、插件机制、私服管理

### 🌐 网络与通信
- **Netty**：NIO/BIO/AIO、事件循环、自定义协议、长连接管理
- **RPC**：gRPC、Dubbo、Thrift 原理与实践
- **CDN**：内容分发原理、静态资源加速策略

### 🔐 认证授权与安全
- 登录体系：Session、JWT、OAuth2、SSO 单点登录
- 认证授权：RBAC/ABAC 模型、Spring Security 集成
- 安全加固：XSS、CSRF、SQL 注入防御、接口签名

### ⚙️ 分布式系统
- **ZooKeeper**：选举机制、分布式协调、配置中心
- **分布式理论**：CAP、BASE、Paxos、Raft
- **分布式事务**：2PC、TCC、Saga、消息最终一致性

### 🏗️ 系统设计与高性能
- 系统设计方法论：拆解、估算、核心组件设计
- **负载均衡**：L4/L7 负载均衡、一致性哈希
- **高性能**：连接池、线程模型、异步化、JVM 调优
- **高可用**：多活架构、容灾备份、故障演练

### 🛡️ 稳定性保障
- **限流**：令牌桶、漏桶、Sentinel 实践
- **熔断与降级**：Hystrix、Resilience4j
- **幂等性**：接口幂等设计、去重方案
- **冗余**：数据冗余、服务冗余策略

### 🐳 容器与云原生
- **Crane**：美团容器调度平台实践
- Docker / Kubernetes 基础与实践

### 🌍 其他后端语言
- **Go**：语法特性、并发模型（Goroutine/Channel）、常用框架（Gin、Gorm）
- **Python**：Flask/FastAPI、数据处理、脚本自动化
- **Node.js**：事件循环、Express/NestJS、全栈场景应用

### 🖥️ 前端技术
- HTML / CSS / JavaScript 基础
- React / Vue 框架实践
- 前后端联调、API 设计

### 🤖 AI 与 Agent 应用开发
- **大模型应用**：Prompt 工程、RAG 检索增强生成
- **Agent 框架**：LangChain、LangGraph、AutoGen
- **AI 工程化**：向量数据库、模型部署、推理优化
- **Java AI 集成**：Spring AI、模型调用封装

---

## 📁 项目结构

> 🚧 **规划中**，后续随学习进度逐步完善补充。

```
java_fullstack_ai_agent_study/
├── README.md                  # 项目说明（当前文件）
├── spring/                    # Spring 全家桶实践
├── databases/                 # 数据库与存储实验
│   ├── mysql/
│   ├── redis/
│   ├── elasticsearch/
│   ├── mongodb/
│   └── hbase/
├── messaging/                 # 消息队列
│   └── kafka/
├── network/                   # 网络与通信
│   ├── netty/
│   └── rpc/
├── security/                  # 认证授权与安全
├── distributed/               # 分布式系统
│   └── zookeeper/
├── system-design/             # 系统设计
├── high-performance/          # 高性能与高可用
├── stability/                 # 稳定性保障（限流/熔断/幂等）
├── cloud-native/              # 容器与云原生
├── other-languages/           # 其他后端语言
│   ├── go/
│   ├── python/
│   └── nodejs/
├── frontend/                  # 前端技术实践
└── ai-agent/                  # AI 与 Agent 应用开发
```

---

## 📝 学习记录

> 后续在此记录各模块的学习进度、踩坑记录、关键结论等。

| 模块 | 状态 | 备注 |
|------|------|------|
| Spring 全家桶 | 🔜 待开始 | |
| MySQL | 🔜 待开始 | |
| Redis | 🔜 待开始 | |
| Kafka | 🔜 待开始 | |
| 系统设计 | 🔜 待开始 | |
| AI/Agent | 🔜 待开始 | |

---

## 🔗 关联项目

| 项目 | 说明 |
|------|------|
| [`java_study`](../java_study) | Java 语言核心 + 计算机基础理论（数据结构、算法、JVM、操作系统、网络等） |
| `java_fullstack_ai_agent_study`（本项目） | 全栈工程实践、架构设计、AI/Agent 应用开发 |

---

*持续更新中 🚀*

