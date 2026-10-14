# 前端选型 + 大厂级高质感 UI 顾问 (frontend-design-advisor v2.1)

> 解决“AI 懂流程但写出的页面依然有廉价模板感”的痛点，将 Linear、Vercel Geist、Stripe、Apple HIG、Raycast 等一线大厂设计系统中的光学物理规律（Optical Physics）、表面海拔体系（Surface Elevation）与微交互动力学（Micro-Physics）转化为 AI 可严格执行的量化硬约束。

---

## ⚡ v2.1 更新：Token 底座落地

v2.0 定下了「Token 底座先行」的原则，v2.1 把它变成可直接复制的文件：

| 新增 | 作用 |
|---|---|
| **templates/tokens.css** | 可复制的设计 Token 底座：暗/浅双主题、4 层海拔表面、Alpha 边框、复合阴影、同心圆角阶梯、动效曲线、间距节奏，附 `.surface-card` / `.glass` / `.hairline-grid` / `.pressable` / `.focus-ring` / `.tnum` 工具类与 `prefers-reduced-motion` 降级。 |
| **templates/tailwind-theme.css** | 把 Token 变量桥接成 Tailwind 原子类（v4 `@theme`，附 v3 等价写法），保证色值只维护一处。 |
| **references/motion-cookbook.md** | 微交互动力学配方库：按压 / 状态切换 / 加载 / 列表入场的具体时长与曲线，外加 6 条动效硬红线。 |
| **CHANGELOG.md** | 版本历史。 |

主流程相应调整：`SKILL.md` 第 5 步现在以 `tokens.css` 起手，动效参数统一从 `motion-cookbook.md` 取。

---

## ⚡ v2.0 大厂级升级核心机制

| 模块 / 文件 | 升级前痛点 | v2.0 大厂级升级核心机制 |
|---|---|---|
| **SKILL.md**（主控流） | 缺乏代码级 Token 契约，AI 写组件易退回默认 gray 类；缺信息密度与光学对齐指令。 | **Token 底座先行机制**：强制先写 `globals.css` / CSS 变量底座再写业务组件；引入 4 档信息密度与 5 态完整度（Default / Hover / Active / Focus-Visible / Skeleton）强制令。 |
| **templates/design-brief.md** | 仅要求 4–6 个平铺 Hex 色值 + 基础圆角，不足以支撑大厂级光影层次。 | 升级为 **4 层表面海拔色板**（Canvas / Surface-1 / Surface-2 / Glass）、Alpha 混合细边框 + 1px 顶部内高光、同心圆角公式与字距光学追踪表。 |
| **references/design-physics.md**（新增） | 缺少底层视觉几何与物理参数规范，AI 凭概率生成间距、阴影和动效时长。 | 沉淀大厂 UI **5 大硬核物理法则**：4 层海拔表面照明、同心圆角几何（$R_{inner} = R_{outer} - Padding$）、字距光学追踪与 tabular-nums、1px 暴露建筑分割线网格、150ms 弹簧阻尼微交互。 |
| **references/style-library.md** | 风格描述偏感性形容词，缺少可直接复制的 CSS/Tailwind 级复合光影配方。 | 为 Linear、Vercel、Stripe、Apple、Notion、飞书 6 大大厂流派补齐精确到 RGBA 的复合表面色阶、Alpha 边框与微光阴影配方。 |
| **references/anti-patterns.md** | 仅拦截表面套路，未拦截深层结构与排版廉价感。 | 新增 **12 条代码级“一眼 AI 味”红线**（禁紫蓝霓虹渐变字、禁纯黑 `#000000`、禁内外同圆角、禁三等分居中图标卡片、禁 300ms 慢缓动、禁大幅上跳）。 |
| **references/quality-checklist.md** | 偏向功能与基础样式检查，缺乏像素级审美验收标准。 | 升级为大厂 **Design QA 4 维 16 项像素级验收单**（表面海拔与光影精度、光学排印与几何对齐、空间节奏与反模板化、交互动力学与全状态覆盖）。 |

---

## 📂 仓库结构

```text
frontend-design-advisor/
├── SKILL.md                          # 顾问主流程控制指令（提问、选型、简报、Token 先行开发、验收）
├── README.md                         # 技能使用说明与版本升级指南
├── CHANGELOG.md                      # 版本更新日志
├── templates/
│   ├── tokens.css                    # 【v2.1 新增】可复制的设计 Token 底座（暗/浅双主题 + 工具类）
│   ├── tailwind-theme.css            # 【v2.1 新增】Token → Tailwind 原子类桥接（v4 @theme，附 v3）
│   └── design-brief.md               # 大厂级设计简报模板（4层海拔色阶、光学字阶、同心圆角、反 AI 审查）
└── references/
    ├── design-physics.md             # 大厂级 UI 光学物理规范（表面光影、几何公式、字体追踪、微动力学）
    ├── motion-cookbook.md            # 【v2.1 新增】微交互动力学配方库与动效硬红线
    ├── style-library.md              # 6 大顶级大厂视觉风格配方（含精确 RGBA Token 与阴影）
    ├── anti-patterns.md              # 12 条反 AI 模板与常见廉价感黑名单
    ├── quality-checklist.md          # 交付前 Design QA 4 维 16 项像素级自检单
    ├── stack-matrix.md               # 现代前端框架、样式与组件生态选型决策矩阵
    └── component-sources.md          # 权威开源组件库、图标库、动效库精选索引
```

---

## 🚀 安装与使用

### 安装目录

把 `frontend-design-advisor/` 目录复制到对应环境：

| 平台 / 环境 | 推荐安装路径 | 生效范围 |
|---|---|---|
| **Google Antigravity** | `~/.gemini/config/skills/frontend-design-advisor/` | 全局可用，自动加载 |
| **Claude Desktop / Code** | `~/.claude/skills/frontend-design-advisor/` | 全局所有项目生效 |
| **CommandCode / ZCode** | `~/.zcode/skills/frontend-design-advisor/` | 全局所有项目生效 |
| **项目级绑定** | 项目根目录 `.claude/skills/` 或 `.gemini/skills/` | 随仓库提交，团队共享 |

### 触发语示例

- 「我想做一个驾考刷题软件」
- 「帮我做个 AI 写作工具，要 Linear 那种高级质感」
- 「要做个企业级数据监控看板，界面不要廉价 AI 味」
- 「前端用什么？页面想要做成大厂设计系统风格」

---

## 🛠️ 如何持续维护知识库

1. **季度核实**：核对 `references/component-sources.md` 里各仓库的星标数与维护状态。
2. **扩充风格库**：遇到惊艳的产品设计，把“对标产品 + 提取的参数（色阶/圆角/字距/光影）”沉淀至 `references/style-library.md`。
3. **沉淀避坑经验**：在实际开发中发现任何廉价感模式，归纳为新红线追加到 `references/anti-patterns.md` 或 `references/motion-cookbook.md`。
4. **记录版本**：任何合并到 `main` 的改动都在 `CHANGELOG.md` 追加条目，并按语义化版本打 tag。