# frontend-design-advisor

「前端选型 + 高质感 UI」技能插件：当你说"我想做个 XXX"，它会用 ≤4 个选项式问题了解需求，给出 1 个最佳 + 1 个备选的技术栈与视觉风格推荐，输出含具体色值/字体/圆角参数的设计简报，再辅助你把页面做成高质感成品，交付前自动按质量清单与反 AI 模板清单自检。

## 目录结构

```
frontend-design-advisor/
├── SKILL.md                  # 触发条件 + 六步工作流程
├── references/
│   ├── stack-matrix.md       # 技术栈决策表
│   ├── style-library.md      # 风格库 + 可落地设计参数
│   ├── component-sources.md  # 组件来源库（含联网核实的 Star 数与维护状态）
│   ├── quality-checklist.md  # 交付前质量清单
│   └── anti-patterns.md      # 反 AI 模板清单
├── templates/
│   └── design-brief.md       # 设计简报模板
└── README.md
```

## 安装

任选其一：

- **个人全局**（所有项目可用）：把 `frontend-design-advisor/` 整个目录放到
  - Claude Code：`~/.claude/skills/frontend-design-advisor/`
  - Command Code：`~/.commandcode/skills/frontend-design-advisor/`
- **仅当前项目**：放到项目根目录 `.claude/skills/`（或 `.commandcode/skills/`），随仓库提交给团队共用。
- 平台不支持 Skills？把 SKILL.md 正文当"系统提示词/自定义指令"用，references 当知识库文件附上。

装完重启会话即可被自动发现；也可用 `/frontend-design-advisor` 手动触发。

## 触发语示例

- 「我想做一个驾考刷题软件」
- 「帮我做个 AI 写作工具」
- 「我要给产品做个宣传首页，要科技感」
- 「前端用什么？页面想要高级一点」

## 如何更新知识库

1. **季度核实**：每 3 个月用 GitHub API 核对 `references/component-sources.md` 中各仓库的 Star 数与维护状态，把"核实于 YYYY-MM"改写为新日期。
2. **扩充风格库**：遇到喜欢的页面，把"对标产品 + 提取的参数（色值/圆角/字体）"追加到 `references/style-library.md`。
3. **记录个人偏好**：多次选择同类风格后，在下方"个人偏好"区记一条，之后默认优先推荐。
4. **反馈迭代**：哪次做得不满意，把原因归纳成新条目写进 `references/anti-patterns.md`。

## 个人偏好

（暂无记录）
