# 开发规范 - {项目名称}

> **文档版本**：v1.0  
> **创建日期**：{日期}  
> **最后更新**：{日期}

---

## 一、代码风格规范

### 1.1 通用规则

- 缩进：2空格
- 引号：单引号
- 分号：不使用分号
- 行宽：100字符

### 1.2 命名约定

| 类型 | 命名规则 | 示例 |
|------|---------|------|
| 变量 | camelCase | `userName` |
| 常量 | UPPER_SNAKE_CASE | `MAX_COUNT` |
| 类/组件 | PascalCase | `UserService` |
| 文件（组件） | PascalCase | `UserProfile.tsx` |
| 文件（工具） | camelCase | `formatDate.ts` |
| 文件（样式） | kebab-case | `user-profile.css` |
| 目录 | kebab-case | `user-management` |

### 1.3 注释规范

```typescript
/**
 * 函数说明
 * @param paramName 参数说明
 * @returns 返回值说明
 */
function functionName(paramName: string): ReturnType {
  // 实现
}
```

---

## 二、Git 规范

### 2.1 分支命名

| 分支类型 | 命名规则 | 示例 |
|---------|---------|------|
| 功能分支 | feature/{功能名} | `feature/user-login` |
| 修复分支 | fix/{问题描述} | `fix/login-error` |
| 重构分支 | refactor/{重构内容} | `refactor/auth-module` |
| 发布分支 | release/{版本号} | `release/v1.0.0` |

### 2.2 提交信息

**格式**：`<type>(<scope>): <subject>`

**类型**：
| 类型 | 说明 |
|------|------|
| feat | 新功能 |
| fix | 修复bug |
| docs | 文档更新 |
| style | 代码格式 |
| refactor | 重构 |
| test | 测试 |
| chore | 构建/工具 |

**示例**：
```
feat(auth): 添加用户登录功能
fix(api): 修复用户数据获取错误
docs(readme): 更新安装说明
```

### 2.3 代码审查

- 所有代码变更必须经过审查
- 审查重点：功能正确性、代码质量、测试覆盖
- 审查通过后方可合并

---

## 三、API 规范

### 3.1 RESTful 设计

| 方法 | 路径 | 说明 |
|------|------|------|
| GET | /api/users | 获取用户列表 |
| POST | /api/users | 创建用户 |
| PUT | /api/users/:id | 更新用户 |
| DELETE | /api/users/:id | 删除用户 |

### 3.2 响应格式

```json
{
  "code": 200,
  "message": "success",
  "data": {}
}
```

### 3.3 错误处理

```json
{
  "code": 400,
  "message": "错误描述",
  "errors": []
}
```

---

## 四、数据库规范

### 4.1 表命名

- 规则：snake_case
- 示例：`user_profiles`、`order_items`

### 4.2 字段命名

- 规则：snake_case
- 示例：`created_at`、`user_name`

### 4.3 索引命名

- 主键：`pk_{表名}`
- 唯一索引：`uk_{表名}_{字段名}`
- 普通索引：`idx_{表名}_{字段名}`

---

## 五、AI 交互协议

### 5.1 Prompt 规范

1. 明确描述目标
2. 提供必要上下文
3. 指定输出格式
4. 提供约束条件

### 5.2 迭代流程

1. 提出需求
2. AI 生成初版
3. 人工审查反馈
4. AI 优化调整
5. 确认定稿

---

**文档维护者**：开发团队  
**最后更新**：{日期}
