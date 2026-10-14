# [产品名称] — 大厂级设计简报 (Design System Brief)

## 1. 产品定位与审美锚点
- 一句话定位：[给谁用 + 解决什么核心问题 + 传递什么气质]
- 视觉风格流派：[风格名称，来自 style-library.md]
- 对标大厂锚点：[例：Linear（暗色海拔与键盘流） + Vercel Geist（1px 建筑感分割线）]
- 信息密度档位：[Compact 高密度工具 / Comfortable 舒适阅读 / Spacious 品牌叙事]

## 2. 表面海拔与语义色板 (Surface Elevation & Semantic Tokens)
- 底层画布 (--bg-canvas)：[例: #08090A]（严禁纯黑 #000000）
- 一级容器 (--bg-surface-1)：[例: #101214]（常规卡片、侧边栏、表格容器）
- 二级悬浮 (--bg-surface-2)：[例: #181B20]（Hover 态、激活项、下拉菜单、代码块）
- 毛玻璃浮层 (--bg-glass)：[例: rgba(16,18,20,0.78) + blur(16px)]
- 一级主文本 (--text-primary)：[例: #F4F4F6]
- 二级副文本 (--text-secondary)：[例: #A1A1AA]
- 三级弱化文本 (--text-muted)：[例: #6E7178]
- 常规细微边框 (--border-subtle)：[例: rgba(255,255,255,0.07)]
- 聚焦/悬浮边框 (--border-strong)：[例: rgba(255,255,255,0.16)]
- 品牌主色 (--accent-primary)：[例: #5E6AD2]（全站面积 ≤ 10%）

## 3. 字体排印与光学阶梯 (Optical Typography Scale)
- 标题字体 (--font-display) / 正文字体 (--font-sans) / 等宽字体 (--font-mono，全局数字强制 tabular-nums)
- Hero (40–52px, line-height 1.10, tracking -0.035em)
- H1 (28–32px, line-height 1.20, tracking -0.025em)
- H2 (20–22px, line-height 1.30, tracking -0.015em)
- Body (14–15px, line-height 1.65, tracking 0em)

## 4. 几何、阴影与动效物理参数 (Geometry & Micro-Physics)
- 同心圆角阶梯：--radius-lg: 14px（外层） / --radius-md: 8px（内嵌与按钮） / --radius-sm: 5px（标签）
- 卡片复合光影 (--shadow-card)：inset 0 1px 0 0 rgba(255,255,255,0.07), 0 1px 2px 0 rgba(0,0,0,0.4), 0 8px 24px -4px rgba(0,0,0,0.35)
- 微交互物理曲线：cubic-bezier(0.22, 1, 0.36, 1)，时长 150ms，按压反馈 active:scale-[0.98]

## 5. 空间布局与 ASCII 架构线框
- 栅格体系与非对称比例说明 + ASCII 结构线框

## 6. 唯一视觉记忆点 (Single Signature Moment)
- 记忆点位置与机制 + 其余区域克制策略

## 7. 反 AI 模板自审记录 (Anti-Cliché Audit)
- 列出本次刻意规避的 3 个 AI 默认俗套做法及替代方案
