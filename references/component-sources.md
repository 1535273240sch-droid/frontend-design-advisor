# 组件与设计参考来源

> 仓库现状均经 GitHub 接口联网核实（核实于 2026-10），星标数会变，仅作量级参考。每季度复核一次。

## 一、界面组件库

| 项目 | 仓库 | 现状（2026-10） | 风格 | 什么时候用 |
|---|---|---|---|---|
| shadcn/ui | shadcn-ui/ui | 约 125k 星标，活跃维护，MIT | 极简克制、深浅自适应、微边框 | **默认首选**：AI 工具、SaaS、作品集 |
| Magic UI | magicuidesign/magicui | 约 22k 星标，活跃维护，MIT | 动态光晕、流光边框、便当盒栅格 | 落地页要"炫"的部分 |
| Aceternity UI | 无官方仓库，组件在官网 ui.aceternity.com 免费复制 | — | 聚光灯、粒子/网格背景、深色科技感 | 同上，偏深色科技风 |
| Ant Design | ant-design/ant-design | 约 100k 星标，活跃维护，MIT | 结构严谨、信息密度高 | 中后台、复杂表单表格 |
| Tabler | tabler/tabler | 约 42k 星标，活跃维护，MIT | 轻量清爽的看板，兼容纯 HTML/CSS 与 React | 数据看板、轻量后台 |
| awesome-design-systems | alexpate/awesome-design-systems | 约 26k 星标，Unlicense，最近更新 2026-04 | 大厂设计规范合集（Polaris、Carbon、Primer 等） | 不知道某组件该怎么定标准时去查 |

## 二、灵感网站

- **Godly.website**：顶尖科技/设计公司官网合集（多为暗色极简、便当盒风）
- **Mobbin.com**：真实 App 与网页界面截图库，按页面类型分类（设置页、注册页、定价表等）

## 三、使用规则

1. 组件优先从 shadcn/ui 取；要炫酷效果**只从 Magic UI / Aceternity 取 1–3 个**，别整页堆砌
2. 中后台优先 Ant Design；风格偏现代 SaaS 则改用 shadcn/ui + TanStack Table
3. 遇到"某交互该怎么设计"，先去 awesome-design-systems 的大厂规范找答案再动手
4. 用户给了参考截图或链接：先提取其配色、圆角、边框、间距、字体特征再落进简报，不要凭感觉模仿
5. 环境里有 shadcn 官方组件服务时，优先用它拉取
6. 使用前确认项目仍在维护、许可证允许，并保留必要的版权声明