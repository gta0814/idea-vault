# AGENTS.md — Global Multi-Agent Protocol & System Contract

> **致所有读取此仓库的 AI 系统（Claude, ChatGPT, Gemini, Grok, Antigravity, 本地 LLM 等）**：  
> 本仓库是项目发起人（GTA0814）所有创新 Idea 与工程原型的 **单一事实来源（Single Source of Truth, SSOT）**。

---

## 1. 核心运行原则 (Core OOP Principles)

1. **状态只读保护（Read-Heavy, Validated-Write）**：
   - 所有的 `ideas/*/README.md` 与技术规范是当前版本的有效状态。
   - 未经用户明确许可，不得单方面篡改核心约束与已有架构决策。
2. **多态角色执行（Polymorphic Execution）**：
   - 无论你是哪一类 AI 引擎，请根据用户指令与你的特长，自动装载对应的角色提示词（Architect, Developer, Patent Attorney, Financial Analyst）。
3. **接口与视图隔离（Interface Segregation）**：
   - 当用户要求你处理某一个特定 Idea 时，**只关注该 Idea 目录下的内容**，不要混淆不同 Idea 之间的名词与上下文。

---

## 2. 目录规范与状态机 (State Machine)

每个 Idea 遵循如下生命周期：
* `Draft`（初始脑暴 / 概念草案）
* `SpecReady`（工业/技术规格与架构完备）
* `PatentPending`（专利交底书准备完成）
* `InDevelopment`（进入代码或硬件打样）
* `Archived`（已归档或商业验证未通过）

---

## 3. 跨平台 AI 协作工作流 (Cross-Platform AI Workflow)

* **Antigravity / IDE Agent**：直接读取本地 `.specs` 与源码，负责高精度的代码实现、仿真计算与文档重构。
* **Grok / Grok BOT**：负责激进的思维碰撞、前沿技术批判性审查（Review）、竞品弱点分析。
* **Gemini (超长窗口)**：负责跨行业论文检索、全量专利数据库交叉比对、长文案白皮书润色。
* **ChatGPT (OpenAI)**：负责通用逻辑梳理、商业模式推演、用户故事编写。
