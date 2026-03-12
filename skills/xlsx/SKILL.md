---
name: "xlsx"
description: "全面的电子表格创建、编辑和分析功能指引，支持公式、格式化、数据分析和可视化。需要处理与电子表格文件(.xlsx, .xlsm, .csv, .tsv 等)相关的任务时使用，包括:(1) 创建带有公式和格式的新电子表格,(2) 读取或分析数据,(3) 修改现有电子表格同时保留公式,(4) 在电子表格中进行数据分析和可视化, (5) 重新计算公式"
---

# XLSX Operations

全面的电子表格操作技能，支持数据处理、公式计算、可视化等操作。

## 触发条件

- 用户需要处理Excel文件
- 用户需要创建电子表格
- 用户需要数据分析
- 用户需要数据可视化

## 核心功能

### 1. 文件操作
- 创建新工作簿
- 读取现有文件
- 保存修改
- 格式转换

### 2. 数据处理
- 读取数据
- 写入数据
- 数据筛选
- 数据排序

### 3. 公式处理
- 添加公式
- 保留现有公式
- 重新计算

### 4. 格式化
- 单元格样式
- 条件格式
- 数据验证
- 冻结窗格

### 5. 数据分析
- 数据透视表
- 统计分析
- 数据聚合

### 6. 可视化
- 创建图表
- 设置图表样式
- 导出图表

## 常用库

```python
import pandas as pd
import openpyxl
from openpyxl import Workbook, load_workbook
from openpyxl.styles import Font, Alignment, PatternFill
from openpyxl.chart import BarChart, LineChart
```

## 操作示例

### 读取数据
```python
import pandas as pd

df = pd.read_excel('data.xlsx', sheet_name='Sheet1')
```

### 创建工作簿
```python
from openpyxl import Workbook

wb = Workbook()
ws = wb.active
ws['A1'] = '标题'
wb.save('output.xlsx')
```

### 添加图表
```python
from openpyxl.chart import BarChart

chart = BarChart()
chart.add_data(ws['A1:B10'])
ws.add_chart(chart, 'D1')
```

## 输出规范

- 保留原有公式
- 保持数据格式
- 支持大数据处理
- 中文路径兼容
