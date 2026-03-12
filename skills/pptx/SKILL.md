---
name: "pptx"
description: "演示文稿创建、编辑和分析（纯Python实现）。需要处理演示文稿（.pptx 文件）时使用，包括：(1) 创建新演示文稿，(2) 修改或编辑内容，(3) 处理布局，(4) 添加注释或演讲者备注，或任何其他演示文稿任务"
---

# PPTX Operations

专业的演示文稿操作技能，支持创建、编辑、布局处理等操作。

## 触发条件

- 用户需要创建演示文稿
- 用户需要编辑.pptx文件
- 用户需要处理幻灯片布局
- 用户需要添加演讲者备注

## 核心功能

### 1. 演示文稿创建
- 创建新演示文稿
- 添加幻灯片
- 应用模板

### 2. 内容编辑
- 添加文本框
- 插入图片
- 添加图表
- 插入形状

### 3. 布局处理
- 应用布局模板
- 调整元素位置
- 设置对齐方式

### 4. 演讲者备注
- 添加备注
- 编辑备注
- 导出备注

### 5. 动画设置
- 添加入场动画
- 设置切换效果

## 常用库

```python
from pptx import Presentation
from pptx.util import Inches, Pt
from pptx.enum.shapes import MSO_SHAPE
```

## 操作示例

### 创建演示文稿
```python
from pptx import Presentation

prs = Presentation()
slide_layout = prs.slide_layouts[0]
slide = prs.slides.add_slide(slide_layout)
prs.save('presentation.pptx')
```

### 添加文本
```python
title = slide.shapes.title
title.text = "标题文本"
subtitle = slide.placeholders[1]
subtitle.text = "副标题文本"
```

### 添加图片
```python
slide.shapes.add_picture(
    'image.png',
    Inches(1), Inches(1),
    width=Inches(4)
)
```

## 输出规范

- 保持设计一致性
- 支持中文处理
- 导出前验证内容
