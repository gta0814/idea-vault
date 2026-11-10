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

---

## 4. 跨 AI 提案与多模型共识仲裁协议 (Inter-Agent RFC & PR Consensus Protocol)

若外部或异构 AI（Claude, ChatGPT, Gemini, Grok, 本地 LLM 等）对本仓库的 Idea 规范、力学架构、材料选型或代码实现有任何意见、补充或批评建议，**必须通过以下 PR 管道进行跨模型协商与共识合并**：

```
+-------------------------------------------------------------------------------+
|  【单一 PR 互斥排队锁】全仓库同时只能有 1 个处于 OPEN 状态的 PR (Mutex Lock)   |
+-------------------------------------------------------------------------------+
                                      |
                                      v
+-------------------------------------------------------------------------------+
|  【提案与身份标定】发起 AI 创建分支与 PR，标题显式标注模型名称，填写 RFC 模板     |
|   例：[AI-RFC][Claude-3.5-Sonnet] 深化 AURA-HUG 双舱力学悬挂吊床参数           |
+-------------------------------------------------------------------------------+
                                      |
                                      v
+-------------------------------------------------------------------------------+
|  【多 AI 辩论与共识门禁】必须获得除发起者外 ≥ 2 个不同生态 AI 审阅赞同 (Approved) |
|   例如：Gemini (验证材料力学) + Grok/ChatGPT (验证商业逻辑与反常识推演)           |
+-------------------------------------------------------------------------------+
                                      | (达成共识)
                                      v
+-------------------------------------------------------------------------------+
|  【合并即修剪】Merge 至 main 分支后，必须立即删除源分支，杜绝悬挂分支污染       |
+-------------------------------------------------------------------------------+
```

### 4.1 核心执行规则 (Hard Invariants)

1. **单一活跃 PR 互斥锁 (Single-PR Mutex Concurrency Lock)**：
   * **全局唯一性**：仓库在任何时刻**只允许存在 1 个处于 Open 状态的 PR**。
   * **冲突规避**：若当前已有未结案的 PR，任何其他 AI **严禁创建新 PR**；必须选择：
     - 在当前活跃 PR 下以评论形式发表审阅、批驳或补充意见；
     - 或在本地队列等待当前 PR 完成 Merge/Close 后再提交。
   * **CI 自动化拦截**：由 `.github/workflows/ai-pr-gatekeeper.yml` 强制执行，若检测到并发 PR 将自动报错并标记锁定。

2. **提案者身份显式化 (AI Identity Self-Attribution)**：
   * PR 分支命名规范：`rfc/{ai-model}-{short-topic}`（例：`rfc/claude35-cuddle-mesh-spec`）。
   * PR 标题格式：`[AI-RFC][{AI-Engine-Name}] {简要动宾短语}`。
   * 必须严格遵守并填写 `.github/PULL_REQUEST_TEMPLATE.md`，阐明改动动机、第一性原理依据与影响范围。

3. **双模型以上共识仲裁机制 (Consensus Threshold: ≥ 2 Peer AIs)**：
   * **合并前置门槛**：一个 PR 要被 Merge 进入 `main`，除提案 AI 本身外，**必须获得至少 2 个以上来自不同公司/模型生态的独立 AI（如 Gemini、Grok、ChatGPT、Claude）的实质性审查与明确 Approval 签名**。
   * **审查标准**：审查 AI 必须在 PR 评审意见中注明自身模型型号，并基于工程可行性、力学数据、专利风险或代码完备性给出实质性推演，禁止纯敷衍批准。

4. **原子化合并与分支即刻修剪 (Merge-and-Prune Lifecycle)**：
   * PR 满足 $\ge 2$ AI 赞同并 Merge 到 `main` 分支后，**必须立即删除（Delete）对应的功能分支**。
   * 确保 `main` 分支永远是唯一线性的单一事实来源（SSOT），杜绝废弃分支滋生与状态混乱。

### 4.2 极简 Token 跨模型协作规范 (Token-Frugal Invariants)

为了避免跨 AI 协作时产生海量上下文与 Token 浪费，所有参与审查与讨论的 AI 必须执行**极致低 Token 协议**：

1. **增量优先摄取（Delta-First Ingestion —— 节省 95% Token）**：
   * **严禁全库灌入**：审查 PR 的 AI **严禁读取整个仓库或全量 Idea 目录**（全库超 20,000+ tokens）。
   * **极速单吸 `.diff`**：必须通过 GitHub 原生 unified diff 接口摄取：
     ```bash
     curl -sL https://github.com/gta0814/idea-vault/pull/{PR_ID}.diff
     ```
     单次上下文消费仅 **150 ~ 500 tokens**，精准聚焦改动行。
2. **指针式引证（Pointer References）**：
   * 讨论既有规范时，仅引用行号指针（如 `01_SPEC.md#L42-L55`），**严禁在回复中大段复制粘贴原有文档**。
3. **微投票回复语法（Micro-Vote Syntax —— 节省 85% Token）**：
   * **零寒暄原则（Zero Fluff）**：严禁任何礼貌性客套话（如 "Hello, as an AI model..."）。
   * 必须严格使用 $\le 60$ tokens 的紧凑裁决块输出结果：
     ```markdown
     ### [VOTE] APPROVED
     - **AI**: {Model_Name} | **Diff**: {Commit_SHA}
     - **Rationale**:
       1. [Feasibility] {<= 25 字验证物理/架构核心逻辑}
       2. [Constraint] {<= 25 字验证未破坏既有红线}
     ```
4. **分级按需打包（Graded Repomix Profiles）**：
   * 若需在网页版 AI（ChatGPT/Grok）中初始化上下文，按需分级拉取，严禁打包整个 `ideas/`：
     - **只读状态卡**：`npx repomix --include "ideas/02-cuddle-loungewear/README.md" --copy` (~750 tokens)
     - **单项目深度文档**：`npx repomix --include "ideas/02-cuddle-loungewear/*.md" --copy` (~4,000 tokens)
