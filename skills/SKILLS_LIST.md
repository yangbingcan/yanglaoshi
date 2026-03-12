# Trae IDE 技能清单

## 本地技能列表（已全部本地化）

| 技能名称 | 描述 | 文件位置 |
|---------|------|---------|
| data-analysis-assistant | 分析 Excel 数据并生成综合 HTML 报告 | `.trae/skills/data-analysis-assistant/SKILL.md` |
| code-reviewer | 代码审查、质量检查、Bug发现、最佳实践建议 | `.trae/skills/code-reviewer/SKILL.md` |
| copywriting | 营销文案撰写（首页/落地页/定价页/功能页） | `.trae/skills/copywriting/SKILL.md` |
| project-planner | 项目规划、里程碑、资源分配、风险管理 | `.trae/skills/project-planner/SKILL.md` |
| test-case-generator | 测试用例生成、边界条件分析、测试场景设计 | `.trae/skills/test-case-generator/SKILL.md` |
| chinese-novelist | 分章节小说创作（10-50章，3000-5000字/章） | `.trae/skills/chinese-novelist/SKILL.md` |
| pdf | PDF文本提取、表格提取、创建、合并/拆分 | `.trae/skills/pdf/SKILL.md` |
| docx | Word文档创建、编辑、修订跟踪、批注处理 | `.trae/skills/docx/SKILL.md` |
| pptx | 演示文稿创建、编辑、布局处理、演讲者备注 | `.trae/skills/pptx/SKILL.md` |
| xlsx | 电子表格创建、编辑、公式、数据分析、可视化 | `.trae/skills/xlsx/SKILL.md` |
| humanizer-zh | 去除AI生成痕迹、文本自然润色 | `.trae/skills/humanizer-zh/SKILL.md` |
| wechat-article | 微信公众号文章创作（浮生风格） | `.trae/skills/wechat-article/SKILL.md` |
| creating-financial-models | DCF分析、敏感性测试、蒙特卡洛模拟、情景规划 | `.trae/skills/creating-financial-models/SKILL.md` |
| prompt-optimize | 提示词工程优化、系统指令改进 | `.trae/skills/prompt-optimize/SKILL.md` |
| brainstorming | 头脑风暴、需求探索、方案发散收敛 | `.trae/skills/brainstorming/SKILL.md` |
| marketing-psychology | 营销心理学原理、思维模型、消费者行为 | `.trae/skills/marketing-psychology/SKILL.md` |
| auto-redbook | 小红书笔记素材创作（标题+正文+图片卡片） | `.trae/skills/auto-redbook/SKILL.md` |
| requirement-analyst | 需求分析、用户故事拆解、功能规划、PRD编写 | `.trae/skills/requirement-analyst/SKILL.md` |
| deep-reading-analyst | 深度阅读分析（SCQA/5W2H/批判性思维等） | `.trae/skills/deep-reading-analyst/SKILL.md` |
| frontend-design-workflow | 前端设计规范、设计到代码工作流 | `.trae/skills/frontend-design-workflow/SKILL.md` |
| jianying-editor | 剪映AI自动化剪辑、字幕生成、视频导出 | `.trae/skills/jianying-editor/SKILL.md` |
| skill-creator | 创建新的自定义技能 | `.trae/skills/skill-creator/SKILL.md` |
| trae-ide-auto-growth-skill-manager | 自动沉淀对话经验、技能迭代优化 | `.trae/skills/trae-ide-auto-growth-skill-manager/SKILL.md` |

---

## 目录结构

```
.trae/
├── rules/
│   └── project_rules.md
└── skills/
    ├── SKILLS_LIST.md
    ├── data-analysis-assistant/
    │   └── SKILL.md
    ├── code-reviewer/
    │   └── SKILL.md
    ├── copywriting/
    │   └── SKILL.md
    ├── project-planner/
    │   └── SKILL.md
    ├── test-case-generator/
    │   └── SKILL.md
    ├── chinese-novelist/
    │   └── SKILL.md
    ├── pdf/
    │   └── SKILL.md
    ├── docx/
    │   └── SKILL.md
    ├── pptx/
    │   └── SKILL.md
    ├── xlsx/
    │   └── SKILL.md
    ├── humanizer-zh/
    │   └── SKILL.md
    ├── wechat-article/
    │   └── SKILL.md
    ├── creating-financial-models/
    │   └── SKILL.md
    ├── prompt-optimize/
    │   └── SKILL.md
    ├── brainstorming/
    │   └── SKILL.md
    ├── marketing-psychology/
    │   └── SKILL.md
    ├── auto-redbook/
    │   └── SKILL.md
    ├── requirement-analyst/
    │   └── SKILL.md
    ├── deep-reading-analyst/
    │   └── SKILL.md
    ├── frontend-design-workflow/
    │   └── SKILL.md
    ├── jianying-editor/
    │   └── SKILL.md
    ├── skill-creator/
    │   └── SKILL.md
    └── trae-ide-auto-growth-skill-manager/
        └── SKILL.md
```

---

## 使用说明

### 本地技能管理
- 技能存放路径：`.trae/skills/技能名称/SKILL.md`
- 修改后可在 Trae IDE 中重新加载生效

### 远程同步
1. 将 `.trae` 目录上传到 Git 仓库
2. 克隆到新环境后，放置到项目根目录
3. 重启 Trae IDE 即可生效

### 技能触发
在对话中明确提及相关需求关键词，技能会自动触发。例如：
- "分析这个Excel" → 触发 data-analysis-assistant
- "帮我写个测试用例" → 触发 test-case-generator
- "优化这个提示词" → 触发 prompt-optimize

---

*清单生成时间: 2026-03-12*
*技能总数: 23个*
