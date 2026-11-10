# 💡 Idea Vault — 跨 AI / Agent 共享创新智库

> **基于面向对象（OOP）思想构建的私有创新状态仓库（Single Source of Truth, SSOT）。**  
> 所有由发起人构思的新 Idea、架构规格与商业方案在此中心化沉淀，并向各种异构 AI 系统（Antigravity、ChatGPT、Gemini、Grok、本地模型）提供标准接口。

---

## 🗂️ Idea 索引列表 (Idea Registry)

| 编号 | Idea 项目名称 | 类别 | 当前状态 | 核心创新点 | 链接 |
| :---: | :--- | :---: | :---: | :--- | :---: |
| **01** | **AEGIS-ORBIT（轨道卫士）** | 户外硬科技 / EDC | `Patent Pending` | 仿空间站太阳能翼四连杆折叠、物理无软线触点安全互锁、3500V 脉冲灭蚊与户外能源集成 | [查看项目](./ideas/01-aegis-orbit/README.md) |
| **02** | **AURA-HUG（云抱服）** | 生物力学 / 智能家居潮服 | `Spec Ready` | 背侧双向力学悬桥手臂减压架构、隐形法式公主线双舱防漏风触控门襟、全柔性日夜全穿 | [查看项目](./ideas/02-cuddle-loungewear/README.md) |

---

## 🤖 跨 AI 读取与同步指南 (How AIs Read This Vault)

### 1. 在 Antigravity / Cursor 等 IDE Agent 中
* 本仓库作为当前工作区，Antigravity 可自动索引所有 `.specs` 与 `ideas/` 下的 Markdown、HTML 及交互组件。
* 任何代码与仿真改动均可通过 Git 进行原子化 Commit。

### 2. 在 ChatGPT / Grok / Gemini 网页版中使用 (极致低 Token 模式)
* **分级按需复制到剪贴板（避免全库 20k+ tokens 冗余）**：
  * **级别 1：快速感知（仅 Idea 状态卡，~750 Tokens）**：
    ```bash
    npx repomix --copy --include "ideas/02-cuddle-loungewear/README.md"
    ```
  * **级别 2：完整白皮书（仅该 Idea 规格与商业案，~5,000 Tokens）**：
    ```bash
    npx repomix --copy --include "ideas/02-cuddle-loungewear/*.md"
    ```
* 直接在聊天框按 `Ctrl+V`，网页端 AI 即可在最低 Token 消耗下掌握关键约束。

### 3. 跨 AI 意见协商与 PR 提案管道 (AI Discussion & RFC Process)
* **严禁私自篡改**：外部 AI 若对任何 Idea 提出建议或质疑，必须通过 Pull Request 进行协商。
* **核心四大原则与极低 Token 规范**：
  1. 🔒 **单一 PR 互斥锁**：全仓库同一时刻**仅允许存在 1 个处于 Open 状态的 PR**，严禁多开；
  2. ⚡ **单吸 Diff 增量（节省 95% Token）**：审阅 PR 时禁止全库输入，直接 `curl -sL <PR_URL>.diff`（仅 ~200 Tokens）；
  3. 🏷️ **身份标定与微投票（节省 85% Token）**：PR 标明 AI 型号，评审 AI 使用 `< 60 Tokens` 的高密裁决语法回帖，零寒暄客套；
  4. ⚖️ **多 AI 共识门禁**：必须获得除发起者外 **≥ 2 个不同生态的独立 AI** 签署 `APPROVED`；
  5. 🧹 **合并即删除**：PR 达成共识 Merge 后，源分支立即删除，维持主干单一事实来源。
* 详见系统契约：[AGENTS.md](./AGENTS.md#4-跨-ai-提案与多模型共识仲裁协议-inter-agent-rfc--pr-consensus-protocol)。

---

## 📐 面向对象架构说明 (Architecture)

```
idea-vault/
├── README.md               # 仓库索引与使用指南
├── AGENTS.md               # 统一 Agent 交互契约与跨 AI 共识仲裁协议
├── repomix.config.json      # 网页端 AI 上下文一键打包配置
├── .github/
│   ├── PULL_REQUEST_TEMPLATE.md     # 跨 AI RFC 提案与多模型仲裁模板
│   └── workflows/
│       └── ai-pr-gatekeeper.yml     # 单一 PR 互斥锁与分支自动修剪 CI
├── .specs/
│   └── TEMPLATE.md         # 新 Idea 创建的标准面向对象模板
└── ideas/
    ├── 01-aegis-orbit/         # 第 1 个 Idea：AEGIS-ORBIT 卫星翼折叠电蚊拍
    │   ├── README.md           # Idea 快速状态卡
    │   ├── 01_SPEC_AND_DESIGN.md   # 工业设计与工程规格白皮书
    │   ├── 02_BUSINESS_AND_PATENT.md # 商业模式、专利权利要求与融资方案
    │   ├── assets/             # 概念渲染图与设计图纸
    │   └── interactive/        # 投资回报计算器与交互组件
    └── 02-cuddle-loungewear/   # 第 2 个 Idea：AURA-HUG 云抱服（手臂分载与双舱隐形触控睡衣）
        ├── README.md           # Idea 状态卡与设计规范速览
        ├── 01_MECHANICAL_AND_TEXTILE_SPEC.md # 生物力学手臂分载、双舱隐形门襟与纺织规格
        └── 02_COMMERCIAL_PATENT_AND_SUPPLY_CHAIN.md # 实用新型专利交底、供应链打板与商业化全案
```
