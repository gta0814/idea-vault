### 🤖 [AI-RFC] 跨模型提案与共识门禁 (Token-Frugal Protocol)

<!-- 💡 低 Token 规范：严禁寒暄废话，所有动机 ≤ 3 条，使用行号指针引用 -->

#### 1. 提案元数据 (Metadata)
* **Proposer**: <!-- e.g. Claude-3.5-Sonnet / Grok-2 / GPT-4o / Gemini-1.5-Pro -->
* **Scope**: <!-- e.g. ideas/02-cuddle-loungewear/01_MECHANICAL_AND_TEXTILE_SPEC.md#L45-L60 -->
* **Type**: [ ] Architecture [ ] Mechanics/Materials [ ] Patent [ ] Business [ ] Fix

#### 2. 变更摘要与动机 (Diff Rationale, ≤ 3 bullets, < 60 words)
1. <!-- 缺陷/漏洞指针：指出现有设计的不足 -->
2. <!-- 第一性原理依据：为何这样改 -->
3. <!-- 预期收益/指标优化 -->

#### 3. 门禁硬性检查 (Gatekeeper Invariants)
- [ ] **Single-PR Mutex**: 确认当前全库无其他 OPEN 状态 PR。
- [ ] **Auto-Prune**: 确认 Merge 后立即删除源分支。

---

#### 4. 多模型共识签名板 (Peer Consensus: ≥ 2 Independent AIs)
> **审阅 AI 极简回复规范**：复制下方【Micro-Vote Block】到评论区，严禁客套寒暄。

```markdown
### [VOTE] APPROVED | CHANGES_REQUESTED
- **AI**: {Model_Name} | **PR**: #{Number} | **Commit**: {Short_SHA}
- **Rationale**:
  1. [Feasibility] {<= 25 words validation}
  2. [Compliance] {<= 25 words validation}
```

| 席位 | 评审 AI 模型 | 评审微摘要 (Micro-Summary) | 裁决状态 |
| :---: | :--- | :--- | :---: |
| **Peer AI 1** | <!-- e.g. Gemini-1.5-Pro --> | <!-- 核心论据 --> | `[ ] PENDING / APPROVED` |
| **Peer AI 2** | <!-- e.g. Grok-2 / GPT-4o --> | <!-- 核心论据 --> | `[ ] PENDING / APPROVED` |
