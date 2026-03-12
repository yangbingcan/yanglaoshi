---
name: "skill-creator"
description: "MANDATORY tool for creating SKILLs - MUST be invoked IMMEDIATELY when user wants to create/add any skill"
---

# Skill Creator

技能创建工具，帮助用户创建新的自定义技能。

## 触发条件

- 用户想要创建新技能
- 用户想要添加自定义技能
- 用户询问如何创建技能

## 技能结构

### 目录结构
```
.trae/skills/<skill-name>/
└── SKILL.md
```

### SKILL.md 格式
```markdown
---
name: "<skill-name>"
description: "<简洁描述，包含功能和触发条件>"
---

# <技能标题>

<详细说明、使用指南、示例>
```

## 必填字段

| 字段 | 位置 | 说明 |
|------|------|------|
| name | frontmatter | 技能唯一标识 |
| description | frontmatter | 功能+触发条件，200字内 |
| detail | body | 完整的markdown内容 |

## 创建步骤

1. **询问技能名称和用途**
2. **生成description字段**：
   - 功能说明
   - 触发条件
   - 默认使用英文
3. **创建目录**：`.trae/skills/<skill-name>/`
4. **创建SKILL.md文件**
5. **验证结构正确**

## 示例

创建 code-reviewer 技能：

```bash
mkdir -p .trae/skills/code-reviewer
```

创建 `.trae/skills/code-reviewer/SKILL.md`：

```markdown
---
name: "code-reviewer"
description: "Reviews code for best practices, bugs, and improvements. Invoke when user asks for code review or before merging changes."
---

# Code Reviewer

This skill reviews code and provides feedback...
```

## 输出格式

```markdown
# 技能创建报告

## 基本信息
- 技能名称：...
- 技能描述：...

## 文件位置
- 目录：.trae/skills/<name>/
- 文件：SKILL.md

## 创建状态
✓ 目录已创建
✓ SKILL.md 已创建
✓ 结构验证通过

## 使用方法
在对话中提及相关关键词即可触发此技能。
```

## 创建原则

1. **名称简洁**：小写字母、连字符
2. **描述清晰**：功能+触发条件
3. **内容完整**：包含使用说明
