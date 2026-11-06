# Caplo Recording Skill

让 Codex 等具备电脑操作能力的 AI 助手与 [Caplo](https://github.com/icloudza/caplo) 联动，录制和编辑 macOS 屏幕演示。需要单独安装 Caplo；本项目不包含 Caplo，也无需 Oil Studio。

## 已测试的功能

- 通过 Caplo 界面开始屏幕录制，并在麦克风、摄像头及系统声音关闭时录制画面。
- 使用 Caplo 的正常退出流程自动结束并保存录制，随后重启 Caplo，在项目中心打开工程。测试环境为 macOS 15.4.1 和 Caplo 0.3.0，全屏录制 13.6 秒，工程保存并可重新打开。
- 在另一次录制测试中通过 Caplo 导出 H.264 MP4，并用 ffprobe 验证文件可读取；录制工程中出现自动聚焦镜头。

结束录制时使用正常退出流程，会关闭 Caplo 窗口，之后需重新打开工程。使用前请确保没有尚未保存的工作或正在进行的导出。不同版本和具体电脑操作工具可能表现不同。

## 尚未完成端到端测试

窗口录制、语音识别、字幕校对、静音清理、语义精剪和带声音的导出尚未完成完整自动化测试。Caplo 本身支持的功能不等于本 Skill 已经验证可自动操作；输出需要检查。

## 使用条件和安装

需要 macOS 15 或以上、[Caplo](https://github.com/icloudza/caplo)、支持电脑界面操作的 AI 助手，以及 macOS 屏幕录制权限。将 `caplo-recording` 文件夹复制到 `~/.codex/skills/`，然后重启 Codex。之后可说：“使用 caplo-recording 录制一个操作演示。”

## 许可和说明

Caplo 的源码和官方安装包采用 PolyForm Noncommercial 许可证，商业用途需另行取得授权，详见 [Caplo 项目](https://github.com/icloudza/caplo)。本项目与 Caplo 官方无隶属关系。
