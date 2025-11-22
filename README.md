# Whisper Command Studio (Web UI)

![界面预览](.github/screenshot.png)

> 一个极简、优雅的 OpenAI Whisper 命令行生成助手。

这是一个单页 Web 应用（Single HTML File），无需服务器，完全在浏览器本地运行。它采用 **Deep Glass (深层毛玻璃)** 设计语言，为您提供了一个可视化的操作界面，将繁琐的 Whisper 命令行操作转化为直观的“拖拽 + 点击”体验。

## ✨ 功能亮点 (Features)

*   **极致美学 (Deep Glass)**：
    *   采用 macOS 原生感的毛玻璃与柔和渐变背景。
    *   丝滑的 UI 动效与呼吸光感反馈。
*   **智能交互 (Smart Interaction)**：
    *   **一体化地址栏**：将输出路径与文件名模式融合，支持实时路径有效性校验。
    *   **视图管理**：代码预览区支持“窄模式/全宽模式”切换，适应不同屏幕空间。
    *   **智能联动**：根据选择的输出格式（SRT/TXT），自动调整输出文件名后缀。
*   **批量处理 (Batch Processing)**：
    *   支持拖拽多个音视频文件，自动生成批量处理脚本。
    *   自动为文件名中的特殊字符（如空格、引号）进行转义。
*   **核心功能**：
    *   **模型选择**：支持 Small, Medium, Large 等模型切换。
    *   **语言指定**：支持自动识别、中文强制、英文强制。
    *   **输出格式**：一键切换纯文本 (TXT) 或 字幕文件 (SRT)。

## 🛠 前置需求 (Prerequisites)

本工具仅用于**生成命令**。要在终端执行生成的命令，您的电脑需要先安装好 OpenAI Whisper 及其依赖环境。

### 1. 安装 FFmpeg (Whisper 的依赖)

**macOS (使用 Homebrew):**
```bash
brew install ffmpeg
```

**Windows (使用 Chocolatey):**
```powershell
choco install ffmpeg
```

**Linux (使用 apt):**
```bash
sudo apt update && sudo apt install ffmpeg
```

### 2. 安装 OpenAI Whisper

您需要 Python 3.8+ 环境。推荐使用 `pip` 进行安装。

```bash
pip install -U openai-whisper
```
更多详细信息，请参考 [OpenAI Whisper 官方仓库](https://github.com/openai/whisper)。

## 🚀 使用方法 (Usage)

1.  **下载 & 打开**: 下载项目中的 `index.html` 文件，用任意现代浏览器（如 Chrome, Safari, Edge）打开它。
2.  **设置输出目录**: 在顶部的地址栏中，粘贴一个**绝对路径**作为输出目录。这是存放转录结果的地方。
3.  **添加媒体文件**: 将你的音视频文件拖拽到“拖入文件”区域，或点击该区域从电脑中选择文件。
4.  **配置转录选项**: 根据需要选择 `Model` (模型), `Lang` (语言), 和 `Format` (输出格式)。
5.  **生成并复制命令**: 右侧会自动生成可执行的 Shell 命令。点击 `复制命令` 按钮。
6.  **执行**: 打开你电脑的终端 (Terminal)，粘贴刚刚复制的命令，然后按回车执行。Whisper 将开始处理你的文件。

## 📄 许可 (License)

本项目采用 [MIT License](LICENSE) 许可。
