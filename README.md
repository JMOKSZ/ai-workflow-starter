# AI Workflow Starter

> **让AI从"自由写代码"变成"按文档跑流水线"**  
> 原作者：[宋宋 @longlongsongs](https://x.com/longlongsongs/status/2063143686016319736)

## 🚀 3分钟上手

### 第一步：贴给AI

把你项目的根目录扔给 **Cursor / Claude Code / Codex**，然后贴这个：

> "先读 `1-onboarding/S01-explore-codebase.md`，按要求执行。"

AI 会自动探索你的代码库，生成 `ARCHITECTURE.md`。

### 第二步：定规矩

把 `2-rules/` 目录里的 `.md` 文件按你的项目改一下，然后告诉 AI：

> "读 `2-rules/` 目录下所有文件，作为你的行为准则。"

### 第三步：开始干活

以后每次开发新功能，按这个顺序走：

| 步骤 | 贴给AI的命令 |
|------|-------------|
| 🅰️ 需求 | "读 `3-skills/S01-demand.md` 并执行" |
| 🅱️ 技术文档 | "读 `3-skills/S02-tech-doc.md` 并执行" |
| 🅲 生成代码 | "读 `3-skills/S03-code-gen.md` 并执行" |
| 🅳 修Bug | "读 `3-skills/S04-bug-fix.md` 并执行" |

---

## 📦 目录结构

```
ai-workflow-starter/
├── 1-onboarding/          # 🎯 让AI先了解项目
│   └── S01-explore-codebase.md
├── 2-rules/               # 📋 行为准则（按需修改）
│   ├── R01-coding-style.md
│   ├── R02-database.md
│   └── R03-conventions.md
├── 3-skills/              # 🧠 4个核心Skill
│   ├── S01-demand.md      # 需求细化
│   ├── S02-tech-doc.md    # 技术文档
│   ├── S03-code-gen.md    # 代码生成（含Harness）
│   └── S04-bug-fix.md     # Bug修复
├── 4-review/              # 🔍 双重复审
│   ├── R01-logical.md
│   └── R02-syntax.md
└── harness/               # ⚙️ 受控流水线（可选）
    └── workflow.md
```

---

## 💡 核心理念

```
        需求文档 ←→❌← 人工确认
              ↓（通过）
        技术文档 ←→❌← 人工确认
              ↓（通过）
    ┌───────Harness（受控流水线）───────┐
    │ AI读架构 + 规则 + 技术文档后写代码  │
    │ → 双重复审（逻辑审 + 语法审）        │
    │ → 自动测试 → PR                    │
    └──────────────────────────────────┘
```

**关键**: 前两关（需求文档 + 技术文档）一定要人工确认。这是时间花得最值的地方。

---

## 🔄 持续迭代

每次翻车 -> 加一条规则到 `2-rules/`  
每次发现架构不清晰 -> 更新 `ARCHITECTURE.md`  
每次Review发现遗漏 -> 更新 `4-review/` 里的检查清单

几个月后，这套东西会成为你的"第二大脑"。

---

> 原帖：[x.com/longlongsongs/status/2063143686016319736](https://x.com/longlongsongs/status/2063143686016319736)  
> 欢迎 Fork、改、PR、一起完善 🎉
