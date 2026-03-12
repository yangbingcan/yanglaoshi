---
name: "pdf"
description: "综合的PDF操作指南，用于提取文本和表格、创建新PDF、合并/拆分文档、处理表单或转换pdf。处理与pdf相关的任务时使用。需要填写PDF表单或以编程方式大规模处理、生成或分析PDF文档时使用。"
---

# PDF Operations

综合的PDF操作技能，支持文本提取、表格处理、文档合并拆分等操作。

## 触发条件

- 用户需要处理PDF文件
- 用户需要提取PDF内容
- 用户需要创建PDF
- 用户需要合并或拆分PDF

## 核心功能

### 1. 文本提取
- 提取全部文本
- 按页面提取
- 保留格式信息

### 2. 表格提取
- 识别表格结构
- 导出为Excel/CSV
- 处理合并单元格

### 3. PDF创建
- 从文本创建
- 从图片创建
- 从HTML创建

### 4. 文档操作
- 合并多个PDF
- 拆分PDF
- 提取特定页面
- 旋转页面

### 5. 表单处理
- 填写表单字段
- 提取表单数据
- 扁平化表单

## 常用库

```python
import PyPDF2
import pdfplumber
import reportlab
from pypdf import PdfReader, PdfWriter
```

## 操作示例

### 提取文本
```python
import pdfplumber

with pdfplumber.open("document.pdf") as pdf:
    for page in pdf.pages:
        text = page.extract_text()
        print(text)
```

### 提取表格
```python
with pdfplumber.open("document.pdf") as pdf:
    for page in pdf.pages:
        tables = page.extract_tables()
        for table in tables:
            # 处理表格数据
            pass
```

### 合并PDF
```python
from pypdf import PdfMerger

merger = PdfMerger()
merger.append("file1.pdf")
merger.append("file2.pdf")
merger.write("merged.pdf")
merger.close()
```

## 输出规范

- 提取内容保持原始结构
- 表格数据导出为结构化格式
- 操作完成后报告处理结果
