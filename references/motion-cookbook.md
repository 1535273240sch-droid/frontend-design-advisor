# 微交互动力学配方库 (Motion Cookbook)

动效是"大厂质感"里最容易露怯的一环：AI 默认爱用 `transition-all duration-300`、大幅上跳和大面积淡入。本库给出可直接抄的参数，全部服从 `design-physics.md` 第 5 条——**高频反馈 140–180ms、单一缓动曲线、零多余动画**。

> 统一缓动：`--ease-out-quint: cubic-bezier(0.22, 1, 0.36, 1)`（快出慢收，瞬时清脆）。
> 需要更"物理"的手感时改用弹簧：`stiffness: 420, damping: 32, mass: 0.8`（Motion / Framer Motion）。
> 所有时长与曲线从 `templates/tokens.css` 取，禁止在组件里现拍数字。

## 1. 反馈与按压（最高频，必须最快）
| 场景 | 参数 | 说明 |
|---|---|---|
| 按钮 Hover | 背景/边框 160ms `ease-out-quint` | 只变背景与边框色，禁止位移 |
| 按钮 Active | `transform: scale(0.98)`，140ms | 一点即到的"按下去"手感 |
| 卡片 Hover | 边框 `--border-subtle → --border-strong`，160ms | **禁止 `-translate-y-2 shadow-2xl` 上跳** |
| 图标按钮 | 同按钮，另加 `stroke-width` 不变 | 图标线宽全站统一，Hover 不改粗细 |

## 2. 状态切换
- **Toggle / Switch**：滑块 160ms `ease-out-quint`；轨道颜色同步过渡，不做弹跳。
- **Tab 指示器**：用滑动指示条（`layoutId` 或 `transform`）160ms 跟随，内容区**做 100ms 极短淡入**而非横向推拉。
- **下拉 / Popover 入场**：`opacity 0→1` + `scale 0.96→1` + `translateY(-4px)→0`，140ms；出场 100ms，方向相反。禁止从远处飞出。
- **Modal / Dialog**：遮罩 `opacity` 160ms；面板 `scale 0.98→1` + `opacity`，160ms。禁止 `scale 0.5` 这种夸张弹入。

## 3. 加载与占位
- **骨架屏 (Skeleton)**：底色 `--bg-surface-2`，叠加 1.4s 无限微光扫过（`linear-gradient` + `translateX`），**不要用刺眼的闪烁**。
- **Spinner**：线性匀速旋转，0.6–0.8s/圈，线宽与图标统一；小尺寸场景优先用骨架屏而非转圈。
- **按钮 Loading**：宽度锁死防抖跳，内部换成 spinner + 文本降级为 60% 透明度。

## 4. 列表与内容入场
- **列表 Stagger**：每项 `opacity 0→1` + `translateY(8px)→0`，140ms，间隔 30–40ms；**超过 8 项只对首屏可见项做**，其余直接渲染。
- **数字变化**：用 `tabular-nums` 配合 240ms 数字滚动/补间，杜绝位宽抖动。
- **图表入场**：路径按 400–600ms 一次画完（`pathLength` / `strokeDashoffset`），只播一次，不循环。

## 5. 唯一视觉记忆点（允许"越界"的唯一区域）
- 全站仅此处可用叙事级动效：首屏编排式入场、滚动视差、光标跟随光晕等。
- 时长可放宽到 400–800ms，但**仍只用同一套缓动**，且必须支持 `prefers-reduced-motion` 降级为直接显示。
- 其余区域保持第 1–4 节的极致克制——记忆点之所以突出，正因为别处安静。

## 6. 硬红线（违反即返工）
- ❌ `transition-all`：必须精确列出过渡属性（`background-color, border-color, transform, opacity`）。
- ❌ 时长 > 200ms 的高频反馈（Hover / Active / Toggle）。
- ❌ 卡片悬浮大幅上跳、`shadow-2xl` 突变。
- ❌ 同一页面混用多种缓动曲线或多种时长节奏。
- ❌ 忽略 `prefers-reduced-motion`。
