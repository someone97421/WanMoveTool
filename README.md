# 🎨 路径绘制小工具

这是一个轻量级的基于 Web 的路径编辑器，专为 **ComfyUI WanMove** 插件及类似工作流设计。它允许用户在参考图上绘制精确的样条曲线，并将其导出为符合特定帧数要求的坐标数据。

---

## 🇨🇳 中文说明

### 核心功能

* **无限画布**：支持平移、缩放，方便在高清参考图上细调路径。
* **双模式编辑**：
* **画笔模式**：像在画板上一样通过鼠标拖拽直接“手绘”路径。
* **编辑模式**：通过点击和拖拽控制点来精细调整路径形状。


* **平滑度控制**：内置 Cardinal Spline 算法，通过 Tension 参数调节路径的圆滑程度。
* **等长重采样**：**（核心特色）** 无论绘制多长，都会根据设置的“总帧数”自动重新采样，确保输出的 JSON 点数完全匹配视频帧数。
* **历史记录**：支持 `Ctrl+Z` 撤销操作。

### 快捷键与操作

* **中键滚轮**：缩放画布。
* **中键拖拽**：移动画布。
* **左键单击/拖拽**：选中或移动控制点。
* **双击路径**：在点击位置增加一个新的控制点。
* **右键点击点**：删除该控制点。
* **Ctrl+Z**：撤销上一步。
* **Delete**：删除当前选中的整条路径。

### 使用流程

1. **上传图片**：点击“选择文件”上传你的视频首帧或参考图。
2. **绘制路径**：点击“进入画笔模式”快速勾勒，或使用“新建曲线”手动点选。
3. **调整参数**：
* 调节 **Tension** 使曲线更平滑或更锐利。
* 设置 **输出总帧数**（需与你 ComfyUI 中的视频帧数设置一致）。


4. **导出**：点击“生成并复制”，JSON 数据会自动进入剪贴板，直接粘贴到 WanMove 节点的输入框即可。

---

## 🇺🇸 English Description

### Core Features

* **Infinite Canvas**: Supports panning and zooming for precise editing on high-resolution reference images.
* **Dual-Mode Editing**:
* **Draw Mode**: "Freehand" path creation by dragging the mouse.
* **Edit Mode**: Fine-tune shapes by clicking and dragging individual control points.


* **Smoothness Control**: Utilizes the Cardinal Spline algorithm with an adjustable **Tension** parameter.
* **Uniform Resampling**: **(Key Feature)** Automatically resamples the path into a fixed number of points based on the "Total Frames" input, ensuring compatibility with ComfyUI node requirements.
* **History System**: Full `Ctrl+Z` undo support.

### Shortcuts & Controls

* **Middle Mouse Scroll**: Zoom in/out.
* **Middle Mouse Drag**: Pan the canvas.
* **Left Click/Drag**: Select or move control points.
* **Double Click on Path**: Insert a new control point at the cursor position.
* **Right Click on Point**: Delete the specific point.
* **Ctrl+Z**: Undo the last action.
* **Delete**: Remove the currently selected curve.

### Workflow

1. **Upload Image**: Click "Choose File" to upload your video's first frame or reference image.
2. **Create Path**: Use "Draw Mode" for quick sketching or "+ New Curve" for manual placement.
3. **Adjust Parameters**:
* Tweak **Tension** for curve smoothness.
* Set **Total Frames** (this must match the frame count in your ComfyUI workflow).


4. **Export**: Click "Generate & Copy." The JSON data is copied to your clipboard instantly, ready to be pasted into the WanMove input field.
