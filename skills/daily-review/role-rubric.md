# 目标岗位能力画像：Agent 应用 / Agent 研发工程师

> **画像背景**：211 本科软件工程 + 1 年工作经验 + Go 主语言（让 AI 写 Python）+ 想做 AI Agent 应用开发，不要模型训练。
> **目标池子**：
> - P0 国内类外企 AI 公司（DeepSeek / 阶跃星辰 / Moonshot / 智谱 / MiniMax / 零一 / 百川）
> - P1 阿里国际 AIDC + 通义新设 AI 岗（出海团队、接近外企）
> - P2 微软中国 + AWS China（真在华外企）
> - 加：京东 TGT 智能体方向（0-2 年极友好）、TikTok Singapore（出海跳板）
> **基础数据**：基于 [real-jds.md](./real-jds.md) 中 45 个真实 JD 整理（2026-05 快照）。
> **本文件可自由修改**，daily-review 按此画像做对标。

---

## 必备硬技能（≥ 80% JD 都要）

### 1. Go 后端工程（你的主战场）
- [ ] 高并发服务（goroutine、channel、context 控制）
- [ ] 流式响应（SSE / WebSocket / gRPC streaming）—— LLM 应用必备
- [ ] 主流 Web 框架（gin / echo / chi 任一）
- [ ] Redis / MySQL / PostgreSQL / Kafka / RabbitMQ
- [ ] 微服务架构、RESTful / gRPC API 设计
- [ ] 限流、重试、熔断、超时控制（生产级 LLM 调用全要）

### 2. Python 协作能力（不需要精通，能 AI 协作写）
- [ ] 读懂主流 Python AI 项目代码（LangChain / LangGraph / FastAPI 源码）
- [ ] 能用 Python 写 prompt / eval 脚本、跑实验
- [ ] async / await 基本理解
- [ ] 包管理与虚拟环境（uv / poetry）

### 3. LLM 应用基础
- [ ] 主流模型 API：Claude / GPT / DeepSeek / Qwen / GLM 任 2-3 个有实战
- [ ] Token 计费、上下文窗口、模型选型 trade-off
- [ ] Prompt 工程：Zero-shot / Few-shot / CoT / ReAct
- [ ] 流式输出处理（含 partial JSON 解析）
- [ ] 错误重试、超时降级、模型 fallback

### 4. Agent 框架（至少一个深度，能讲 loop 内部机制）
- [ ] **LangChain / LangGraph / AutoGen / Dify / Coze 任一**深度使用
- [ ] **能讲清楚 Agent loop**：何时调工具、何时反思、何时退出
- [ ] Function Calling / Tool Use 设计（含**工具权限设计与失败回退**）
- [ ] 至少跑通过一个**端到端非 demo 项目**

### 5. RAG 系统
- [ ] 向量数据库使用（Milvus / Qdrant / Chroma 任一）
- [ ] Embedding 模型选型（bge / m3e / openai-embedding-3）
- [ ] 检索策略：混合检索（BM25 + 向量）、Reranking
- [ ] Chunking 策略、Context 压缩
- [ ] **接入业务数据**的完整链路（清洗 → 向量化 → 检索 → 生成）

### 6. Eval 体系建设（**1 年经验最容易缺**，重点补）
- [ ] **Curated dataset** 设计与维护
- [ ] **LLM-as-judge** 模式与 prompt 设计
- [ ] Offline replay（用真实流量回放测试）
- [ ] Regression alert / 自动化评测 pipeline
- [ ] 把模糊质量问题翻译成具体 metric

### 7. 生产部署 & 工程化（**1 年经验也容易缺**）
- [ ] Docker / K8s 基础（含 **Helm chart**）
- [ ] CI/CD pipeline
- [ ] **可观测性**：日志（结构化）+ 指标（Prometheus）+ 链路追踪（OpenTelemetry）
- [ ] LLM 调用监控（LangSmith / LangFuse / 自研埋点）
- [ ] **成本监控**：能讲"我把单次 query 成本从 X 降到 Y"

---

## 关键加分（50-80% JD 要求）

### 8. Multi-Agent 协作
- [ ] 多 Agent 任务规划与调度
- [ ] Agent 间通信（共享 memory / message bus）
- [ ] Workflow 引擎设计（节点 + 边 + 触发器）
- [ ] 插件系统设计

### 9. Memory 工程化
- [ ] 短期 memory（对话上下文压缩）
- [ ] 长期 memory（Redis + 向量库 + TTL + 召回策略）
- [ ] 工作记忆与语义记忆区分

### 10. Cost / Latency 优化
- [ ] **小模型分流**：简单查询走小模型，复杂走大模型
- [ ] **Auto 模型选择**（参考 Cursor 设计）
- [ ] Prompt Caching 应用
- [ ] 并发批处理
- [ ] 流式输出加速首 token

### 11. A/B 测试 & 灰度
- [ ] 线上实验框架基本理解
- [ ] 灰度发布、分流策略
- [ ] 指标定义与显著性判断

---

## 差异化加分（< 50% JD，但能拉开差距）

### 12. MCP（Model Context Protocol）
- [ ] MCP server 实现经验
- [ ] sub-agent / agent skill 设计
- [ ] 这是 Anthropic / DeepSeek / 腾讯广告 显性要求，**上升期热词**

### 13. Tool Use 安全
- [ ] Least privilege 工具权限设计
- [ ] Sandboxed execution（如 Docker / WASM 隔离）
- [ ] Prompt injection 防护
- [ ] 输出过滤与审核

### 14. 国际化业务（针对 P1/P2 池子）
- [ ] 多语言 / 多地区适配
- [ ] 跨境数据合规基础（GDPR 概念）
- [ ] 时区、币种、地区差异处理

---

## 软技能（外企 / 出海 BU 隐形必备）

- [ ] **英文异步写作**（Notion / Linear / GitHub Issue 风格）
- [ ] 技术文档（设计文档、复盘文档）
- [ ] 跨团队协作（产品、算法、前端、海外团队）
- [ ] 公开技术分享（博客 / 演讲 / GitHub）

---

## 🔥 加分项（决定能否突破"3+ 年门槛"和"硕士偏好"）

> 这是你**用 1 年经验 + 211 本科**冲破隐形门槛的关键武器。

### A. 真实上线项目（**Top 1 武器**）
- [ ] **至少 1 个端到端、有用户的 Agent / RAG / LLM 应用项目**
- [ ] 不是 toy demo，要有**真实数据**：用户数 / 调用量 / 准确率 / 成本数字
- [ ] 公开 GitHub 仓库 + 详细 README + 部署链接
- [ ] 写一篇技术博客讲清楚架构选型

### B. Vibe Coding 重度用户证据（**已显性化为加分项**）
- [ ] **深度使用 Claude Code / Cursor / Devin / Manus** 至少一个
- [ ] 能讲清楚每个工具的**优劣对比** + **与自己代码风格的契合度**
- [ ] 在 GitHub / X / 知乎写过相关博客或 demo

### C. 开源贡献
- [ ] **首选**：给 LangChain / LangGraph / Dify / Coze / vLLM 等主流仓库提 PR
- [ ] **次选**：自己独立项目 ≥ 100 star
- [ ] **基础**：在 Issue 区有持续高质量讨论

### D. 论文阅读积累
- [ ] 能复述 ReAct / Reflexion / Constitutional AI / MCP spec
- [ ] 关注 Anthropic blog、OpenAI blog、arxiv 周更
- [ ] **不要求自己发 paper**，但要能讲清楚关键技术

### E. 客户面向 / FDE 思维（针对外企）
- [ ] 能把模糊需求拆成可执行子任务
- [ ] 在客户系统中构建 PoC 的能力
- [ ] 写 playbook 的习惯

### F. 成本数字（**面试关键问题**）
- [ ] "我把 X 场景成本从 ¥A 降到 ¥B" 这类硬数字
- [ ] 知道每个模型的 input / output token 价格

### G. 对前沿模型有"taste"
- [ ] 能讲清楚 Claude 4 vs GPT-5 vs DeepSeek V3 的实际差异
- [ ] 知道什么场景该选什么模型
- [ ] 关注主流 leaderboard（SWE-bench、AgentBench、Tau-bench）

---

## 🚫 显式不需要的（基于你的目标排除）

> 这些是大厂算法岗 / 研究岗常见要求，**你的目标岗位不要求**，时间不要花在这里。

- ❌ 模型预训练（pretraining）
- ❌ SFT / RLHF / DPO 等微调技术细节
- ❌ LoRA / QLoRA / Adapter 等参数高效微调
- ❌ PyTorch 分布式训练（DDP / FSDP / DeepSpeed）
- ❌ 模型架构创新（Attention 变种、MoE 等）
- ❌ 强化学习算法（除非作为加分，但优先级低）
- ❌ NLP 顶会论文要求（你的目标岗不卡）
- ❌ 985 硕士同等学力要求（目标池都不卡）

---

## 🎯 1 年经验 → 目标岗位的 Top 5 关键卡点

排序后的"必须先补"清单（基于真实 JD 共性分析）：

1. **真实上线的 Agent 项目** —— 用户级 / 内部生产级 demo + 数据；卡掉 80% 同水平候选人
2. **Eval 体系建设** —— Curated dataset + scorer + dashboard 闭环讲一遍
3. **LangChain / LangGraph 等任一框架的内部机制** —— 不只会用 API，能讲 Agent loop
4. **生产成本硬数字** —— "我把单次 query 成本从 X 降到 Y"
5. **后端工程化基本功** —— K8s / 可观测性 / 微服务（你 Go 主语言这块本来就是优势）

---

## 📝 简历对标参考结构（写简历时按此组织）

### 项目级
- [ ] 端到端做过的 Agent / RAG / LLM 应用项目
- [ ] 一句话描述 + 2-3 个量化指标（调用量 / 准确率 / 成本 / 延迟）
- [ ] 公开 GitHub / 部署链接

### 能力级
- [ ] **熟练使用**：[Go / Python / Agent 框架 / 向量库 / K8s，每个有项目实战]
- [ ] **深度理解**：[Agent loop / RAG 检索策略 / Eval 设计 / 成本优化，能讲清楚为什么]
- [ ] **了解**：[MCP / 多模态 / 微调，用过但不深入]

### 量化成果
- [ ] 性能：latency P50/P99
- [ ] 成本：单次 query / 月度成本节省
- [ ] 准确率：召回率、人工评分、用户反馈
- [ ] 规模：用户数 / 调用量 / 数据量

### 开源 / 影响力
- [ ] GitHub 仓库 / star 数 / fork 数
- [ ] PR 到主流仓库
- [ ] 技术博客 / 总阅读量
- [ ] 公开演讲 / Meetup

### 工具栈使用证据
- [ ] Claude Code / Cursor / Devin 等使用感受与博客
- [ ] 自己造的 dev tools / agent skills

---

## 🔄 daily-review 使用此画像的方式

每次 `/daily-review` 时按以下方式对标：

1. 今日工作触及了哪些**必备技能**条目？
2. 今日工作触及了哪些**加分项**条目？特别注意 🔥 Top 1 武器（真实项目）
3. 今日是否暴露 **Top 5 卡点**中的任何一个？
4. 今日有没有产出**简历级量化指标**？

如果连续 3 天都没触及 🔥 Top 1 武器（真实上线项目），daily-review 应该警告"主线产出停滞"。
