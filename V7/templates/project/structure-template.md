# 项目结构 - {项目名称}

> **文档版本**：v1.0  
> **创建日期**：{日期}  
> **最后更新**：{日期}

---

## 一、目录结构

```
{项目根目录}/
├── src/                # 源代码
│   ├── ...
├── tests/              # 测试文件
├── docs/               # 文档
├── public/             # 静态资源
└── ...
```

---

## 二、目录说明

| 目录 | 用途 | 说明 |
|------|------|------|
| src/ | 源代码 | 主要开发目录 |
| tests/ | 测试文件 | 单元测试、集成测试 |
| docs/ | 文档 | 项目文档 |
| public/ | 静态资源 | 静态文件 |

---

## 三、命名规范

### 3.1 目录命名

- 规则：kebab-case
- 示例：`user-management`、`api-service`

### 3.2 文件命名

| 文件类型 | 命名规则 | 示例 |
|---------|---------|------|
| 组件文件 | PascalCase | `UserProfile.tsx` |
| 工具文件 | camelCase | `formatDate.ts` |
| 样式文件 | kebab-case | `user-profile.css` |
| 配置文件 | kebab-case | `vite.config.ts` |

### 3.3 变量命名

| 类型 | 命名规则 | 示例 |
|------|---------|------|
| 变量 | camelCase | `userName` |
| 常量 | UPPER_SNAKE_CASE | `MAX_COUNT` |
| 类/接口 | PascalCase | `UserService` |
| 函数 | camelCase | `getUserById` |

---

## 四、模块划分

### 4.1 模块结构

```
{模块名}/
├── index.ts            # 模块入口
├── types.ts            # 类型定义
├── service.ts          # 服务层
├── controller.ts       # 控制器
└── tests/              # 测试文件
```

### 4.2 模块依赖

{描述模块间的依赖关系}

---

## 五、文件组织原则

### 5.1 按功能划分

{描述按功能划分的原则}

### 5.2 按类型划分

{描述按类型划分的原则}

---

**文档维护者**：开发团队  
**最后更新**：{日期}
