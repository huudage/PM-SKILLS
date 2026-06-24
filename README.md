# PM-SKILLS

产品经理相关的 AI agent skills 集合。

## Skills

### [`prd-0to1-ai`](./prd-0to1-ai/SKILL.md)
从 0 到 1 构建 AI / RAG 产品 PRD 的工作流 skill。

特点：
- **分模块增量构建**：5 个固定模块 + 8 个按需纳入的可选模块。
- **对话驱动 / 缺口优先**：只就缺失且影响质量的信息主动追问，不臆测填空。
- **两个项目本地看板**：
  - 长期记忆看板（事实 / 偏好 / 指代）
  - 构建现状看板（进度 / 计划 / 决策门）
- **决策门**：方向性取舍交用户拍板，而非替用户决定。
- **可中断恢复**：凭两个看板还原上下文继续。

固定模块：
1. 产品目标与范围（Why/How/What + 目标用户与场景）
2. 核心工作流与目的
3. AI 核心人设（系统提示词 / 对话逻辑 / CoT）
4. 前端设计 + 后端架构（含字段清单）
5. 异常处理与兜底策略

目录结构：
```
prd-0to1-ai/
├── SKILL.md
└── templates/
    ├── board-A-memory.md     # 长期记忆看板模板
    ├── board-B-status.md     # 构建现状看板模板
    └── prd-skeleton.md       # 成品 PRD 骨架
```

## 安装（Claude Code）

将某个 skill 目录放到项目的 `.claude/skills/` 或用户级 `~/.claude/skills/` 下即可被发现。
