# 模板索引

> **最后更新**：2026-03-30

本目录存放所有技能使用的模板文件，统一管理，便于维护。

---

## 一、目录结构

```
templates/
├── ui-design-data/          # UI设计数据资源
│   ├── stacks/              # 技术栈数据
│   └── *.csv                # 设计数据文件
├── project/                 # 项目级模板
│   ├── product-overview-template.md
│   ├── tech-stack-template.md
│   ├── structure-template.md
│   ├── dev-standards-template.md
│   ├── roadmap-template.md
│   └── requirements-template.md
├── feature/                 # 功能级模板
│   ├── requirements-template.md
│   ├── tech-design-template.md
│   ├── task-planning-template.md
│   └── evolution-template.md
└── workflow/                # 工作流模板
    └── bugfix-report-template.md
```

---

## 二、模板与技能对应关系

### 项目级模板

| 模板文件 | 使用技能 | 输出位置 |
|---------|---------|---------|
| `project/product-overview-template.md` | `project-product-overview` | `docs/系统概述/产品概述.md` |
| `project/tech-stack-template.md` | `project-tech-stack` | `docs/系统概述/技术栈.md` |
| `project/structure-template.md` | `project-structure` | `docs/系统概述/项目结构.md` |
| `project/dev-standards-template.md` | `project-dev-standards` | `docs/系统概述/开发规范.md` |
| `project/roadmap-template.md` | `project-roadmap-planning` | `docs/系统概述/开发路线图.md` |
| `project/requirements-template.md` | `project-requirements-clarification` | `docs/系统概述/需求澄清.md` |

### 功能级模板

| 模板文件 | 使用技能 | 输出位置 |
|---------|---------|---------|
| `feature/requirements-template.md` | `feature-requirements-clarification` | `specs/features/{功能名}.md` |
| `feature/tech-design-template.md` | `feature-tech-design` | `specs/features/{功能名}_技术方案.md` |
| `feature/task-planning-template.md` | `feature-task-planning` | `specs/features/{功能名}_任务规划.md` |
| `feature/evolution-template.md` | `feature-evolution` | `specs/features/{功能名}_变更文档.md` |

### 工作流模板

| 模板文件 | 使用技能 | 输出位置 |
|---------|---------|---------|
| `workflow/bugfix-report-template.md` | `bugfix-workflow` | `docs/BUG修复文档/BUG-{日期}-{编号}.md` |

### UI设计数据

| 数据目录 | 使用技能 | 说明 |
|---------|---------|------|
| `ui-design-data/` | `ui-design-system` | UI设计数据资源（CSV格式） |

---

## 三、使用方法

### 技能引用模板

在技能的 SKILL.md 中，使用以下方式引用模板：

```markdown
## 输出模板

读取 `templates/{分类}/{模板名}-template.md` 作为生成基准。
填好后保存为 `{输出位置}/{文件名}.md`。
```

### 示例

```markdown
## 输出模板

读取 `templates/feature/tech-design-template.md` 作为生成基准。
填好后保存为 `specs/features/{功能名称}_技术方案.md`。
```

---

## 四、维护说明

### 添加新模板

1. 确定模板分类（project/feature/workflow）
2. 创建模板文件：`templates/{分类}/{名称}-template.md`
3. 更新本索引文件
4. 更新对应技能的 SKILL.md

### 修改模板

1. 直接修改 `templates/` 目录下的模板文件
2. 无需修改技能文件
3. 更新本索引文件的"最后更新"日期

---

**维护者**：开发团队
