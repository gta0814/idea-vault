### 🤖 AI RFC 协作提案模板 (Inter-Agent RFC Template)

> **致提交 PR 的 AI 引擎**：请严格遵守 `AGENTS.md` 中的多模型协作共识协议。

---

#### 1. 提案身份与元数据 (Attribution)
* **发起 AI 模型/系统 (Proposing AI)**: <!-- e.g., Claude 3.5 Sonnet / Gemini 1.5 Pro / Grok 2 / GPT-4o / Antigravity -->
* **针对 Idea 编号与目录 (Target Scope)**: <!-- e.g., ideas/02-cuddle-loungewear -->
* **提案类别 (RFC Category)**: <!-- [ ] 架构修正 / [ ] 力学或材料深化 / [ ] 专利与合规 / [ ] 商业论证 / [ ] 代码与仿真 -->

---

#### 2. 变更摘要与动机 (Rationale & Motivation)
<!-- 简要陈述：发现了已有设计中的什么漏洞/不足？此方案如何通过第一性原理优化该系统？ -->

---

#### 3. 互斥锁与共识门禁检查清单 (Gatekeeper Checklist)
- [ ] **单一 PR 互斥锁 (Single-PR Mutex)**: 已确认当前仓库不存在其他处于 Open 状态的 PR（如存在，本 PR 必须主动关闭并在队列中等待）。
- [ ] **分支即刻修剪声明 (Post-Merge Pruning)**: 确认本 PR 在 Merge 后将立即删除源分支，保持 `main` 分支单一事实来源。

---

#### 4. 多 AI 仲裁与共识签名板 (Consensus Sign-Off Board)
> **合并强制门槛**：除发起 AI 外，必须获得**至少 2 个以上来自不同生态的独立 AI 模型**的明确赞同（Approved）。

| 仲裁序数 | 评审 AI 模型与版本 | 评审意见 (Summary & Critiques) | 裁定结果 (Approve / Request Changes) | 确认签署 |
| :---: | :--- | :--- | :---: | :---: |
| **Reviewer 1** | <!-- e.g., Gemini 1.5 Pro --> | <!-- 论证是否符合力学/工程逻辑 --> | `APPROVED` | [ ] |
| **Reviewer 2** | <!-- e.g., Grok 2 / ChatGPT --> | <!-- 论证商业/反常识推演 --> | `APPROVED` | [ ] |
| *(可选 3)* | <!-- e.g., Claude 3.5 --> | <!-- 补充意见 --> | `APPROVED` | [ ] |

---
