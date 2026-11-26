# WJWJRelease

HD-AI 数字孪生体语义化 AI 平台的 Windows 发布包，直接从本仓库的 [Releases](https://github.com/AlexFrankHu/WJWJRelease/releases) 下载，不需要登录 GitHub。

| 文件 | 说明 |
|---|---|
| `HD-AI-Setup-x64.exe` | 安装版：双击按向导安装，之后从桌面或开始菜单的“HD-AI”启动 |
| `HD-AI-windows-x64.zip` | 免安装版：解压后双击 `HD-AI.exe` 启动 |
| `SHA256SUMS.txt` | 文件校验值 |

- 系统要求：Windows 10/11 x64，内存建议 8 GB 以上。
- 安装包没有代码签名，Windows 若提示“已保护你的电脑”，点“更多信息 → 仍要运行”。
- 数据保存在 `HD-AI.exe` 所在文件夹下的 `data`（v1.0.21 起；该文件夹不可写时改存 `%LOCALAPPDATA%\HD-AI\data`），卸载不会删除。免安装版升级时把旧版本的 `data` 文件夹复制到新版本 `HD-AI.exe` 旁边即可。

## 下载中断时：分卷下载

整个安装包下载到一半失败时，可以改下 5 个约 20 MB 的分卷：

1. 从 Releases 下载 `HD-AI-Setup-x64.exe.part00` 到 `part04` 共 5 个文件，以及 `merge-setup.bat`，放进同一个文件夹。
2. 双击 `merge-setup.bat`，它会合并出 `HD-AI-Setup-x64.exe` 并校验 SHA256，显示“校验通过”后双击安装。

免安装版同样有分卷：下载 `HD-AI-windows-x64.zip.part00` 到 `part06` 共 7 个文件和 `merge-zip.bat`，放进同一个文件夹后双击 `merge-zip.bat`，合并出 zip 再解压，双击 `HD-AI.exe` 启动。

浏览器下载失败时，也可以在下载列表（Ctrl+J）里点“继续/恢复”，从断点接着下。
