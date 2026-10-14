# 大厂级 UI 光学与物理规范 (Design Physics & Optical Rules)

普通页面与大厂出品（Linear、Vercel、Stripe、Apple、Raycast）的差距，90% 不在配色本身，而在表面海拔光影、几何圆角比例、字体光学微调、以及动力学反馈。所有前端代码必须执行以下 5 条硬性物理法则。

## 1. 表面海拔与照明法则 (Surface Elevation & Specular Lighting)
- 深色模式 (Dark Mode) 黄金法则：
  - 禁止纯黑与死灰：底层画布用深邃冷曜石色（如 #08090A 或 #0A0A0C），绝不用纯 #000000。
  - 越靠近用户的层级越亮：
    - Level 0 (Canvas)：#08090A
    - Level 1 (Card / Sidebar)：#101214 或 rgba(255, 255, 255, 0.03)
    - Level 2 (Elevated / Hover / Modal)：#16191D 或 rgba(255, 255, 255, 0.06)
    - Level 3 (Glass Floating)：rgba(22, 25, 29, 0.75) + backdrop-filter: blur(16px) saturate(180%)
  - Alpha 边框 + 顶部内高光：
    - 边框永远用 1px solid rgba(255, 255, 255, 0.07)（Hover 时升至 0.14）。
    - 卡片与主按钮叠加顶部微高光：box-shadow: inset 0 1px 0 0 rgba(255, 255, 255, 0.08), 0 4px 20px -2px rgba(0, 0, 0, 0.5);
- 浅色模式 (Light Mode) 黄金法则：
  - 当卡片是纯白 #FFFFFF 时，底层画布微灰（#F8F9FA 或 #F4F4F5），或采用 Vercel 式纯白画布 + 1px solid rgba(0, 0, 0, 0.08) 建筑分割网格。
  - 多层环境光阴影：box-shadow: 0 0 0 1px rgba(0, 0, 0, 0.06), 0 1px 2px -1px rgba(0, 0, 0, 0.06), 0 8px 24px -4px rgba(0, 0, 0, 0.04);

## 2. 同心圆角几何公式 (Concentric Border Radius)
嵌套容器内外圆角严禁相等，必须执行公式：Inner Radius = max(4px, Outer Radius - Padding)
- 外层 16px (rounded-2xl) + 内边距 8px (p-2) -> 内层 8px (rounded-lg)
- 外层 12px (rounded-xl) + 内边距 4px (p-1) -> 内层 8px (rounded-lg)
- 外层 10px + 内边距 4px (p-1) -> 内层 6px (rounded-md)

## 3. 字体光学追踪与混排法则 (Optical Typography)
- 字号越大，字距越紧；字号越小（全大写），字距越宽：
  - Hero / H1 (32px–56px)：letter-spacing: -0.03em ~ -0.04em，line-height: 1.1 ~ 1.15
  - H2 / Section Title (20px–28px)：letter-spacing: -0.02em，line-height: 1.25
  - Body 正文 (14px–16px)：中文 line-height: 1.65 ~ 1.75，英文 1.5 ~ 1.6
  - Eyebrow / 眉题小标签 (11px–12px 大写)：letter-spacing: 0.06em ~ 0.08em，font-weight: 600
- 数字与表格强制等宽对齐：所有金额、统计卡片、百分比、时间戳、表格列必须加 font-variant-numeric: tabular-nums。
- 文本灰度阶梯：Text-Primary (100%) / Text-Secondary (65%–72%) / Text-Muted (45%–50%)。
- 最佳阅读行宽：正文段落单行宽度严格限制在 60ch–72ch。

## 4. 建筑感布局与非对称节奏 (Architectural Grid & Rhythm)
- 禁止“三等分居中图标卡片”连续堆叠，改用非对称 Bento Grid（如 7:5 + 4:8）或左文右交互舞台（4:8）。
- 1px 暴露网格线（Exposed Hairline Grid）：外层 bg-border gap-px border border-border，内层格 bg-surface-0 p-6，形成精密 1px 通栏分割线。
- 宏观留白 > 微观留白（至少 3 倍差距）：元素内间距 8px–12px，卡片内边距 20px–28px，大模块间距 64px–112px。

## 5. 微交互动力学参数 (Micro-Physics & Easing)
- 高频反馈时长控制在 140ms–180ms，使用 cubic-bezier(0.22, 1, 0.36, 1) 或 Spring (stiffness: 420, damping: 32, mass: 0.8)。
- 按钮点击态：active:scale-[0.98]；卡片悬浮态严禁大幅度上跳，仅做边框提亮与背景微亮。

具体到每个交互场景（按压 / 状态切换 / 加载 / 列表入场）的时长、曲线与红线，见 references/motion-cookbook.md。
