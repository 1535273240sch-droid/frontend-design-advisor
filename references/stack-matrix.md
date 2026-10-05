# 技术栈决策表

> 原则：选主流、生态大、AI 最熟的方案——这样后续让 AI 迭代时出错率最低。版本号以官方文档为准，此处只写方向。

## 按产品类型

| 产品类型 | 最佳推荐 | 备选 | 说明 |
|---|---|---|---|
| 官网 / 落地页 | Next.js + Tailwind + shadcn/ui + Magic UI（或 Aceternity UI）+ Motion | Astro（纯静态、极致加载速度） | 要炫酷动效用 Magic UI / Aceternity 现成效果 |
| AI 工具 / SaaS | Next.js（或 Vite + React）+ Tailwind + shadcn/ui | Vue 3 + Nuxt + Tailwind | 风格对标 Linear / Vercel |
| 后台管理 | React + Ant Design（国内首选） | shadcn/ui + TanStack Table；或 Tabler（轻量） | 表单表格多时 Ant Design 效率最高 |
| 数据看板 | React + Tailwind + shadcn/ui + Recharts（或 ECharts） | Tabler 看板模板 | 国内图表需求多优先 ECharts |
| 桌面软件 | Tauri + React + Tailwind + shadcn/ui | Electron（需兼容大量 Node 生态时） | Tauri 体积小、启动快 |
| 手机网页 | React/Vite + Tailwind + PWA | Vue 3 + Vant | 最省事，无需应用商店 |
| 手机 App | Expo（React Native） | Flutter | 与 Web 共用 React 经验 |
| 小程序 | uni-app（Vue 3） | 原生小程序 / Taro | 一套代码多端 |
| 作品集 / 博客 | Astro 或 Next.js + Tailwind + shadcn/ui | — | 内容为主，克制排版 |
| 文档站 | Astro Starlight 或 Docusaurus | Nextra | 不要自己造轮子 |

## 按用户情况微调

- 完全不懂编程、全程让 AI 写 → 选 Next.js 或 Vite + React（AI 语料最多），避开冷门框架
- 只在本机用、不联网 → 倾向 Tauri 或单页 Vite 应用，别上服务器
- 需要登录 / 数据库 → 加 Supabase 或 PocketBase，省去自建后端
- 国内用户为主 → 用系统字体栈或自托管字体，避免被墙的 CDN
- 需要多语言 → 一开始就接 i18n（next-intl / vue-i18n），后补很痛苦

## 通用默认

- 语言 TypeScript；样式 Tailwind CSS，颜色/圆角/字体走设计变量
- 图标 Lucide（与 shadcn/ui 默认搭配）；包管理 pnpm
- 动效用 Motion（原 Framer Motion），纯 CSS 能解决的不引库