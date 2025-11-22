# Whisper Command Studio (Web UI)

![界面预览](screenshot.png)

> 一个极简、优雅的 OpenAI Whisper 命令行生成助手。

这是一个单页 Web 应用（Single HTML File），无需服务器，完全在浏览器本地运行。它采用 **Deep Glass (深层毛玻璃)** 设计语言，为您提供了一个可视化的操作界面，将繁琐的 Whisper 命令行操作转化为直观的“拖拽 + 点击”体验。

## ✨ 功能亮点 (Features)

* **极致美学 (Deep Glass)**：
    * 采用 macOS 原生感的毛玻璃与柔和渐变背景。
    * 丝滑的 UI 动效与呼吸光感反馈。
* **智能交互 (Smart Interaction)**：
    * **一体化地址栏**：将输出路径与文件名模式融合，支持实时正则校验。
    * **视图管理**：代码预览区支持“窄模式/全宽模式”切换，适应不同屏幕空间。
    * **智能联动**：根据选择的输出格式（SRT/TXT），自动调整输出文件名后缀。
* **批量处理 (Batch Processing)**：
    * 支持拖拽多个音视频文件，自动生成批量处理脚本。
    * 自动转义文件名中的特殊字符（空格、引号等）。
* **核心功能**：
    * **模型选择**：支持 Small, Medium, Large 等模型切换。
    * **语言指定**：支持自动识别、中文强制、英文强制。
    * **输出格式**：一键切换纯文本 (TXT) 或 字幕文件 (SRT)。

## 🛠 前置需求 (Prerequisites)

本工具仅用于**生成命令**。要在终端执行生成的命令，您的电脑需要安装 OpenAI Whisper 环境。

### 1. 安装 FFmpeg (Whisper 的依赖)
**macOS:**
```bash
brew install ffmpeg
