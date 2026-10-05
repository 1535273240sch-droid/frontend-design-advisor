# 技术栈决策表

> 原则：选主流、生态大、AI 最熟悉的方案——这样后续让 AI 继续迭代时出错率最低。
> 版本号开发时以官方文档为准，此处只写方向。

## 一、按产品类型选

| 产品类型 | 最佳推荐 | 备选 | 说明 |
|---|---|---|---|
| 官网 / 落地页 / 宣传页 | Next.js + Tailwind CSS + shadcn/ui + Magic UI（或 Aceternity UI）+ Motion | Astro（纯静态、要极致加载速度） | 要炫酷动效，用 Magic UI / Aceternity 的现成效果 |
| AI 工具 / 现代 SaaS | Next.js（或 Vite + React）+ Tailwind + shadcn/ui | Vue 3 + Nuxt + Tailwind | 风格对标 Linear / Vercel |
| 后台管理 / 企业系统 | React + Ant Design（国内业务首选） | shadcn/ui + TanStack Table；或 Tabler（偏纯 HTML/轻量） | 表单、表格多时 Ant Design 效率最高 |
| 数据看板 / 仪表盘 | React + Tailwind + shadcn/ui + Recharts（或 ECharts） | Tabler 的 Dashboard 模板 | 图表国内需求多时优先 ECharts |
| 桌面软件（电脑端） | Tauri + React + Tailwind + shadcn/ui | Electron（要兼容大量 Node 生态时） | Tauri 体积小、启动快 |
| 手机 H5 / 可添加到桌面 | React/Vite + Tailwind + PWA 方案 | Vue 3 + Vant | 最省事，无需应用商店 |
| 手机 App | Expo（React Native） | Flutter | 与 Web 技术栈共用 React 经验 |
| 小程序 | uni-app（Vue 3） | 原生小程序 / Taro | 一套代码多端 |
| 个人作品集 / 博客 | Astro 或 Next.js + Tailwind + shadcn/ui | — | 内容为主，克制排版 |
| 纯阅读 / 文档站 | Astro Starlight 或 Docusaurus | Nextra | 不要自己造轮子 |

## 二、按用户情况微调

- 用户完全不会编程、全程让 AI 写 → 选 Next.js 或 Vite + React（AI 训练语料最多），避免冷门框架。
- 只在本机使用、无需联网 → 倾向 Tauri 桌面软件或单页 Vite 应用，避免上服务器。
- 需要登录 / 数据库 → 追加推荐：Supabase 或 PocketBase（省去自建后端）。
- 国内用户为主 → 注意字体加载（用系统字体栈或自托管字体）、避免依赖被墙的 CDN。
- 需要多语言 → 一开始就接入 i18n（如 next-intl / vue-i18n），后补很痛苦。

## 三、通用默认项

- 语言：TypeScript
- 样式：Tailwind CSS，颜色/圆角/字体统一走设计变量
- 图标：Lucide（与 shadcn/ui 默认搭配）
- 包管理：pnpm
- 动效：Motion（原 Framer Motion）用于 React；纯 CSS 能解决的不引库
