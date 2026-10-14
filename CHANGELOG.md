# 更新日志 (Changelog)

本项目遵循 [语义化版本](https://semver.org/lang/zh-CN/)。

## v2.1.0 — 2026-10-14

让 v2.0 提出的「Token 底座先行」从口号变成可复制落地的文件。

### 新增
- **`templates/tokens.css`** — 可直接复制的设计 Token 底座：暗/浅双主题、4 层海拔表面、Alpha 边框、复合阴影、同心圆角阶梯、动效曲线、间距节奏，以及 `.surface-card` / `.glass` / `.hairline-grid` / `.pressable` / `.focus-ring` / `.tnum` 等工具类。含 `prefers-reduced-motion` 降级。
- **`templates/tailwind-theme.css`** — 把 Token 变量桥接成 Tailwind 原子类（v4 `@theme inline`），并附 v3 `tailwind.config` 等价写法，保证"色值只在一处"。
- **`references/motion-cookbook.md`** — 微交互动力学配方库：按压/状态切换/加载/列表入场的具体时长与曲线，以及 6 条动效硬红线。补齐此前动效仅有 2 行说明的空白。
- **`CHANGELOG.md`** — 本文件。

### 变更
- `SKILL.md` 第 5 步改为**先复制 `templates/tokens.css` 作为底座**，并接入 `motion-cookbook.md` 的动效参数；提问工具名由泛称 `ask_user_question` 修正为 `AskUserQuestion`（ZCode 实际工具名），保留无该工具时的编号列表兜底。
- `README.md` 版本与目录结构同步更新。

## v2.0.0 — 2026-10-14

大厂级审美规范体系升级：把 Linear / Vercel / Stripe / Apple / Raycast 的光学物理规律转成 AI 可执行的量化硬约束。

### 新增
- `references/design-physics.md` — 5 大物理法则（4 层海拔照明、同心圆角公式、光学字距与 tabular-nums、1px 暴露网格、150ms 弹簧微交互）。
- `references/anti-patterns.md` — 12 条代码级"一眼 AI 味"红线。

### 变更
- `templates/design-brief.md` 升级为 4 层海拔色板 + Alpha 边框 + 光学字阶 + 反 AI 自审。
- `references/style-library.md` 为 6 大流派补齐精确到 RGBA 的复合表面色阶与阴影配方。
- `references/quality-checklist.md` 升级为 4 维 16 项像素级验收单。

## v1.0.1 — 2026-10-05

- 全部文档改为中文并精简（-244 行）。

## v1.0.0 — 2026-10-05

- 首个版本：前端技术选型 + 高质感 UI 技能插件（选型矩阵、风格库、组件来源、设计简报模板）。
