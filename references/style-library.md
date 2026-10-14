# 大厂级视觉风格配方库 (Big-Tech Style Archetypes)

## 1. Linear / Raycast 暗黑精密工业风 (Dark Precision Craft)
- 适用：AI 工具、开发者产品、效率软件、高频生产力工作台
- Token：--bg-canvas: #08090A | --bg-surface-1: #101214 | --bg-surface-2: #17191C | --bg-glass: rgba(16,18,20,0.75) + blur(16px)
- 文本与边框：--text-primary: #F4F5F8 | --text-secondary: #9599A3 | --border-subtle: rgba(255,255,255,0.07) | --accent-primary: #5E6AD2
- 招牌阴影：inset 0 1px 0 0 rgba(255,255,255,0.09), 0 4px 16px -2px rgba(0,0,0,0.5)

## 2. Vercel Geist 瑞士国际主义建筑网格 (Architectural Monochrome Grid)
- 适用：SaaS 官网、云平台控制台、数据监控看板、技术文档
- Token：--bg-canvas: #FAFAFA | --bg-surface-1: #FFFFFF | --bg-surface-2: #F4F4F5 | --text-primary: #09090B | --border-subtle: #E4E4E7
- 招牌技法：用暴露的 1px 纵横通栏分割线（Exposed Hairlines）代替独立阴影卡片，交界处点缀 7px "+" 号准星。

## 3. Stripe 弥散流光与多层白卡 (Luminous Layered FinTech)
- 适用：金融科技、企业级 SaaS、支付结算后台、高信任度商业首页
- Token：--bg-canvas: #F6F9FC | --bg-surface-1: #FFFFFF | --text-primary: #0A2540（深海藏青黑） | --accent-primary: #635BFF
- 招牌阴影：0 0 0 1px rgba(10,37,64,0.05), 0 2px 4px rgba(10,37,64,0.04), 0 12px 28px -4px rgba(10,37,64,0.08)

## 4. Apple HIG / Craft 原生温润材质风 (Tactile Native & Translucent Glass)
- 适用：消费级应用、效率笔记、教育刷题工具、iOS/macOS 风格 Web App
- Token：--bg-canvas: #F5F5F7 | --bg-surface-1: #FFFFFF | --bg-glass: rgba(255,255,255,0.72) + saturate(180%) blur(20px) | --accent-primary: #0071E3
- 圆角：大卡片 20px，内部模块 12px，分段控制器外 10px / 内 7px

## 5. Notion / Readwise 温暖人文社论风 (Warm Editorial & Knowledge)
- 适用：AI 写作工具、知识库、阅读器、个人博客与深度内容平台
- Token：--bg-canvas: #FBF9F5 | --bg-surface-1: #F4F0EA | --text-primary: #191918 | --accent-primary: #D95D39
- 字体：标题使用人文衬线体（Newsreader / Songti SC），正文使用无衬线体

## 6. 飞书 / Arco Design 高效企业生产力风 (High-Density Enterprise Workspace)
- 适用：B 端复杂业务中台、CRM/ERP、多维表格、高密度数据分析系统
- Token：--bg-canvas: #F2F3F5 | --bg-surface-1: #FFFFFF | --text-primary: #1D2129 | --border-subtle: #E5E6EB | --accent-primary: #165DFF
