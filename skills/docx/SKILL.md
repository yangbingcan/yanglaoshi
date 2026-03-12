---
name: "docx"
description: "全面的word(.docx)文档创建、编辑和分析功能，支持修订跟踪、批注、格式保留和文本提取。处理与word文档（.docx 文件）相关的任务时使用，包括：(1) 创建新文档，(2) 修改或编辑内容，(3) 处理修订跟踪，(4) 添加批注，或任何其他文档任务"
---

# DOCX Operations

全面的Word文档操作技能，支持创建、编辑、格式处理等操作。

## 触发条件

- 用户需要创建Word文档
- 用户需要编辑.docx文件
- 用户需要处理修订跟踪
- 用户需要添加批注

## 核心功能

### 1. 文档创建
- 创建新文档
- 添加标题、段落
- 插入图片、表格
- 设置页面格式

### 2. 内容编辑
- 查找替换
- 段落操作
- 样式修改
- 格式调整

### 3. 修订跟踪
- 开启修订模式
- 接受/拒绝修订
- 查看修订历史

### 4. 批注处理
- 添加批注
- 删除批注
- 回复批注

### 5. 文档分析
- 提取文本
- 获取文档结构
- 统计字数

## 常用库

```python
from docx import Document
from docx.shared import Inches, Pt
from docx.enum.text import WD_ALIGN_PARAGRAPH
```

## 操作示例

### 创建文档
```python
from docx import Document

doc = Document()
doc.add_heading('标题', level=1)
doc.add_paragraph('正文内容')
doc.save('document.docx')
```

### 添加表格
```python
table = doc.add_table(rows=3, cols=3)
for row in table.rows:
    for cell in row.cells:
        cell.text = '内容'
```

### 设置样式
```python
paragraph = doc.add_paragraph()
run = paragraph.add_run('文本')
run.bold = True
run.font.size = Pt(14)
```

## 输出规范

- 保持原有格式
- 支持中文处理
- 操作完成后验证结果
