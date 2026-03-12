---
name: "jianying-editor"
description: "剪映 (JianYing) AI自动化剪辑的高级封装 API (JyWrapper)。提供开箱即用的 Python 接口，支持录屏、素材导入、字幕生成、Web 动效合成及项目导出。当用户想要自动化视频编辑、生成草稿或在剪映专业版中操作媒体资源时使用此技能。"
---

# JianYing Editor

剪映AI自动化剪辑技能，支持视频编辑自动化。

## 触发条件

- 用户需要自动化视频编辑
- 用户需要生成剪映草稿
- 用户需要在剪映中操作媒体资源

## 核心功能

### 1. 录屏功能
- 屏幕录制
- 区域选择
- 音频捕获

### 2. 素材导入
- 视频导入
- 图片导入
- 音频导入
- 批量处理

### 3. 字幕生成
- 语音识别
- 字幕添加
- 样式设置
- 时间轴对齐

### 4. Web动效合成
- 动画效果
- 转场效果
- 特效添加

### 5. 项目导出
- 格式选择
- 分辨率设置
- 导出配置

## 常用操作

### 创建项目
```python
from jy_wrapper import JianYing

jy = JianYing()
project = jy.create_project("我的项目")
```

### 导入素材
```python
project.import_media("video.mp4")
project.import_media("image.png")
project.import_media("audio.mp3")
```

### 添加字幕
```python
project.add_subtitle(
    text="字幕内容",
    start_time=0,
    end_time=5,
    style="default"
)
```

### 导出项目
```python
project.export(
    output_path="output.mp4",
    resolution="1080p"
)
```

## 输出格式

```markdown
# 剪映自动化报告

## 执行操作
- 创建项目：✓
- 导入素材：✓
- 添加字幕：✓
- 导出视频：✓

## 输出文件
- 路径：...
- 格式：...
- 时长：...

## 注意事项
- ...
```

## 使用原则

1. **确保剪映已安装**
2. **素材路径正确**
3. **导出前预览**
