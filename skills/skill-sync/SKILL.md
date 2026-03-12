---
name: "skill-sync"
description: "技能同步管理工具，用于将本地技能推送到远程Git仓库或从远程仓库下载覆盖本地。当用户需要同步技能、推送技能到仓库、从仓库下载技能时使用。"
---

# Skill Sync

技能同步管理工具，支持本地技能与远程 Git 仓库的双向同步。

## 触发条件

- 用户需要推送技能到远程仓库
- 用户需要从远程仓库下载技能
- 用户需要同步技能配置

## 配置说明

### 默认远程仓库
- 仓库地址：`https://github.com/yangbingcan/yanglaoshi.git`
- 技能目录：`.trae/skills/`
- 规则目录：`.trae/rules/`

## 功能模块

### 1. 推送技能到远程仓库

将本地技能推送到 Git 远程仓库。

**操作步骤**：
```bash
# 进入 .trae 目录
cd .trae

# 初始化仓库（如果未初始化）
git init

# 添加远程仓库（如果未添加）
git remote add origin https://github.com/yangbingcan/yanglaoshi.git

# 添加所有更改
git add .

# 提交更改
git commit -m "Update skills"

# 重命名分支为 main
git branch -M main

# 推送到远程
git push -u origin main
```

**PowerShell 命令**：
```powershell
Set-Location ".trae"
git init
git remote add origin https://github.com/yangbingcan/yanglaoshi.git
git add .
git commit -m "Update skills"
git branch -M main
git push -u origin main
```

### 2. 从远程仓库下载技能

从 Git 远程仓库克隆技能到本地。

**操作步骤**：
```bash
# 备份现有技能（可选）
mv .trae .trae_backup

# 克隆仓库到 .trae 目录
git clone https://github.com/yangbingcan/yanglaoshi.git .trae
```

**PowerShell 命令**：
```powershell
# 备份现有技能
Rename-Item ".trae" ".trae_backup" -ErrorAction SilentlyContinue

# 克隆仓库
git clone https://github.com/yangbingcan/yanglaoshi.git .trae
```

### 3. 更新本地技能

拉取远程最新更改。

```bash
cd .trae
git pull origin main
```

## 输出格式

```markdown
# 技能同步报告

## 操作类型
- 推送 / 下载 / 更新

## 执行结果
| 步骤 | 状态 |
|------|------|
| git init | ✓ |
| git remote add | ✓ |
| git add | ✓ |
| git commit | ✓ |
| git push/pull | ✓ |

## 同步文件
- 新增：X 个
- 修改：Y 个
- 删除：Z 个

## 远程仓库
- 地址：https://github.com/yangbingcan/yanglaoshi.git
- 分支：main
```

## 注意事项

1. **推送前检查**：确保已保存所有更改
2. **下载前备份**：建议备份现有 .trae 目录
3. **冲突处理**：如有冲突需手动解决
4. **权限验证**：推送需要 Git 认证

## 快捷命令

### 推送技能
```
推送技能到仓库 / push skills / 上传技能
```

### 下载技能
```
从仓库下载技能 / pull skills / 下载技能 / 同步技能
```

## 技能目录结构

```
.trae/
├── .git/                          # Git 仓库
├── rules/
│   └── project_rules.md           # 项目规则
└── skills/
    ├── SKILLS_LIST.md             # 技能清单
    ├── skill-sync/
    │   └── SKILL.md               # 本技能
    ├── data-analysis-assistant/
    ├── code-reviewer/
    └── ...                        # 其他技能
```

## 错误处理

### 推送失败
- 检查网络连接
- 验证 Git 认证
- 确认仓库权限

### 下载失败
- 检查仓库地址是否正确
- 确认仓库是否存在
- 检查本地目录权限

### 冲突解决
```bash
# 查看冲突文件
git status

# 手动解决后
git add .
git commit -m "Resolve conflicts"
git push
```
