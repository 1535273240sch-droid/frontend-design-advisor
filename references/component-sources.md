# 组件与设计参考来源

> 以下仓库现状均经 GitHub API 联网核实（核实于 2026-10），Star 数会持续变化，仅作量级参考。
> 每季度应重新核实一次（见 README"如何更新知识库"）。

## A. 前端 UI 组件 / 设计标杆（GitHub）

| 项目 | 仓库 | 现状（核实于 2026-10） | 风格特征 | 什么时候用 |
|---|---|---|---|---|
| shadcn/ui | shadcn-ui/ui | 约 125k Star，活跃维护，MIT | 极简克制、深浅自适应、微边框，现代 SaaS 主流审美 | **默认首选**：AI 工具、SaaS、作品集、技术型工具 |
| Magic UI | magicuidesign/magicui | 约 22k Star，活跃维护，MIT | 动态光晕、流光边框、Bento Grid、动效卡片 | 落地页、官网首页要"炫"的部分 |
| Aceternity UI | 无官方开源仓库，组件在官网 ui.aceternity.com 免费复制（核实于 2026-10） | —（非开源仓库） | Spotlight、粒子/网格背景、深色科技感 | 同上，偏深色科技风；官网直接复制代码 |
| Ant Design | ant-design/ant-design | 约 100k Star，活跃维护，MIT | 结构严谨、信息密度高 | 中后台、复杂表单与表格 |
| Tabler | tabler/tabler | 约 42k Star，活跃维护，MIT | 轻量、清爽的 Dashboard，支持纯 HTML/CSS 与 React | 数据看板、轻量后台 |
| awesome-design-systems | alexpate/awesome-design-systems | 约 26k Star，Unlicense，最近更新 2026-04 | 全球大厂设计规范合集（Polaris、Carbon、Primer 等） | 不知道某组件（按钮、弹窗、表单）该怎么定标准时去查 |

## B. 灵感与参考网站（让用户/AI 对着截图复刻风格）

- Godly.website：顶尖科技/设计公司官网合集（多为 Linear / Bento 风格）
- Mobbin.com：真实 App 与 Web 界面截图库，按页面类型分类（设置页、注册页、定价表等）

## C. 使用规则

1. 组件优先从 shadcn/ui 取；需要炫酷效果时，**只从 Magic UI / Aceternity 取 1–3 个**，不要整页堆砌。
2. 中后台优先 Ant Design；如果用户风格偏现代 SaaS，改用 shadcn/ui + TanStack Table。
3. 遇到"某个交互该怎么设计"的问题，先到 awesome-design-systems 里的大厂规范找答案，再动手。
4. 用户给了参考截图或链接时：先提取其配色、圆角、边框、间距、字体特征，再落到简报里，不要凭感觉模仿。
5. 如果环境里有 shadcn 官方 MCP / registry，优先用它拉取组件。
6. 每次使用前确认项目仍在维护、许可证允许使用；组件代码保留必要的版权声明。
