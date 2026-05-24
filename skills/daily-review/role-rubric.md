# 目标岗位能力画像：大厂 AI Agent 开发

> 基于 2025-2026 字节 / 阿里 / 腾讯 / 美团 / 百度 / 拼多多 等大厂 AI Agent、LLM 应用工程岗 JD 整理。
> **本文件可自由修改**，daily-review skill 会按此画像做对标。
> 修改后下次 /daily-review 自动生效。

---

## A. 核心技术能力

### A1. LLM 应用基础
- [ ] 熟悉主流模型 API（OpenAI / Anthropic / 文心 / 通义 / 智谱 / DeepSeek 等）
- [ ] 理解 token 计费、上下文窗口、不同模型的能力 trade-off
- [ ] Prompt 工程：Zero-shot / Few-shot / CoT / ReAct / Self-consistency
- [ ] 流式输出、错误重试、超时处理、降级策略
- [ ] Prompt Caching 等成本优化机制

### A2. Agent 框架与开发
- [ ] LangChain / LlamaIndex 至少一个深度使用经验
- [ ] Function Calling / Tool Use 设计与实现
- [ ] Multi-agent 框架（AutoGen / CrewAI / LangGraph）
- [ ] 国内平台：Coze / Dify / 字节 Coze Studio / 百炼
- [ ] Claude Agent SDK / OpenAI Assistants API

### A3. RAG 系统
- [ ] 向量数据库选型与使用（Milvus / Pinecone / Qdrant / Chroma / Weaviate）
- [ ] Embedding 模型选型（bge / m3e / openai-embedding-3）
- [ ] 检索策略：混合检索、Reranking、HyDE、Query Rewriting
- [ ] Chunking 策略、Context 压缩、多模态 RAG

### A4. Agent 高阶能力
- [ ] Memory 设计：短期 / 长期 / 语义 / 工作记忆
- [ ] Planning：任务拆解、Plan-and-Execute、ReAct
- [ ] Self-reflection / Self-correction / Critique
- [ ] Cost / Latency 优化（小模型分流、Cache、并发）
- [ ] 安全与对齐：jailbreak 防护、prompt injection、输出过滤

### A5. 评估与监控
- [ ] Eval 集设计与自动化评测
- [ ] 回归测试、A/B 测试、灰度发布
- [ ] LLM 调用监控（LangSmith / LangFuse / 自研埋点）
- [ ] Hallucination 检测与缓解

---

## B. 工程能力

### B1. Python 工程
- [ ] async / await、类型注解、单元测试
- [ ] FastAPI / Flask 后端服务
- [ ] 依赖管理（uv / poetry / pip-tools）
- [ ] 代码质量：mypy / ruff / pytest

### B2. 系统与基础设施
- [ ] Docker / K8s 基础
- [ ] 消息队列（Kafka / RabbitMQ / Redis Stream）
- [ ] 缓存（Redis）、数据库（PostgreSQL / MySQL）
- [ ] 微服务架构、API 设计

### B3. 数据能力
- [ ] SQL 熟练度
- [ ] 数据清洗 / ETL 基础
- [ ] 简单的数据可视化（看指标、做报表）

---

## C. 业务与软技能

- [ ] 模糊需求拆解为可执行子任务
- [ ] 找业务痛点的能力（用户访谈、数据驱动）
- [ ] 技术文档写作（设计文档、复盘文档）
- [ ] 英文论文阅读（关注 arxiv、Anthropic blog、OpenAI blog）
- [ ] 跨团队协作（产品、算法、前端）

---

## D. 加分项

- [ ] **GitHub 开源贡献**：独立项目（带 star）/ 给主流仓库的 PR
- [ ] **端到端 Agent 项目**：跑通过非 demo 级的真实系统
- [ ] **论文积累**：能复述近期重要 paper（ReAct / Reflexion / AutoGen / RAG-survey / Constitutional AI）
- [ ] **Cost-aware 设计**：实际优化过 LLM 调用成本，有数据支撑
- [ ] **行业影响力**：技术博客 / 演讲 / 公开分享
- [ ] **英文能力**：阅读 / 写作 / 与海外社区互动

---

## E. 简历对标参考结构

> daily-review 提取简历素材时，按下面结构尝试归类

### 项目级
- 端到端做过的 Agent / RAG / LLM 应用项目（一句话描述 + 1-2 个量化指标）

### 能力级
- 熟练使用：[工具/框架列表，每个有实际使用经验]
- 深度理解：[原理性内容，能讲清楚为什么的]
- 了解：[用过但不深入的]

### 量化成果
- 性能优化：latency / cost / accuracy 提升的具体数字
- 规模：用户数 / 调用量 / 数据量

### 开源 / 影响力
- GitHub 仓库 / star 数
- 技术博客 / 总阅读量
