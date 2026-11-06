# 💡 Idea Vault — 跨 AI / Agent 共享创新智库

> **基于面向对象（OOP）思想构建的私有创新状态仓库（Single Source of Truth, SSOT）。**  
> 所有由发起人构思的新 Idea、架构规格与商业方案在此中心化沉淀，并向各种异构 AI 系统（Antigravity、ChatGPT、Gemini、Grok、本地模型）提供标准接口。

---

## 🗂️ Idea 索引列表 (Idea Registry)

| 编号 | Idea 项目名称 | 类别 | 当前状态 | 核心创新点 | 链接 |
| :---: | :--- | :---: | :---: | :--- | :---: |
| **01** | **AEGIS-ORBIT（轨道卫士）** | 户外硬科技 / EDC | `Patent Pending` | 仿空间站太阳能翼四连杆折叠、物理无软线触点安全互锁、3500V 脉冲灭蚊与户外能源集成 | [查看项目](./ideas/01-aegis-orbit/README.md) |

---

## 🤖 跨 AI 读取与同步指南 (How AIs Read This Vault)

### 1. 在 Antigravity / Cursor 等 IDE Agent 中
* 本仓库作为当前工作区，Antigravity 可自动索引所有 `.specs` 与 `ideas/` 下的 Markdown、HTML 及交互组件。
* 任何代码与仿真改动均可通过 Git 进行原子化 Commit。

### 2. 在 ChatGPT / Grok / Gemini 网页版中使用
* **一键复制全量上下文到剪贴板**：
  在项目根目录下运行：
  ```bash
  npx repomix --copy --include "ideas/01-aegis-orbit/**"
  ```
* 直接在聊天框按 `Ctrl+V`，任何网页端 AI 均可瞬间同步该 Idea 的完整规格与设计约束。

---

## 📐 面向对象架构说明 (Architecture)

```
idea-vault/
├── README.md               # 仓库索引与使用指南
├── AGENTS.md               # 统一 Agent 交互系统契约
├── repomix.config.json      # 网页端 AI 上下文一键打包配置
├── .specs/
│   └── TEMPLATE.md         # 新 Idea 创建的标准面向对象模板
└── ideas/
    └── 01-aegis-orbit/     # 第一个 Idea 实战用例
        ├── README.md       # Idea 快速状态卡
        ├── 01_SPEC_AND_DESIGN.md   # 工业设计与工程规格白皮书
        ├── 02_BUSINESS_AND_PATENT.md # 商业模式、专利权利要求与融资方案
        ├── assets/         # 概念渲染图与设计图纸
        └── interactive/    # 投资回报计算器与交互组件
```
