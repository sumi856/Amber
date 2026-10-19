# Amber（公开资产仓库）

这是 Amber 桌面下载器的**公开构建资产与说明仓库**，不包含应用源码。

## 这里有什么

| 内容 | 位置 | 说明 |
| --- | --- | --- |
| Amber 下载助手（Chrome / Edge 扩展） | Releases 中标签以 `browser-extension-v` 开头的版本 | 独立安装包；优先使用最新的扩展包 |
| 微信视频号取件扩展 | Releases 中标签以 `weixin-channels-v` 开头的版本 | 应用内「从 GitHub 安装」读取这个渠道 |
| macOS 本地语音引擎 | Release `engine-whisper-macos-arm64` | whisper-cli 资产 |
| 隐私政策 | [PRIVACY.md](PRIVACY.md) | 扩展如何处理页面信息、媒体地址和本地数据 |
| 使用支持 | [SUPPORT.md](SUPPORT.md) | 安装、常见问题和反馈方式 |

## 浏览器扩展

Amber 下载助手是 Amber 桌面应用的浏览器入口。扩展本身不下载视频，需要在本机安装并运行 Amber 0.6.2 或更新版本。

- 进入 [Releases](https://github.com/sumi856/Amber/releases)，选择标签以 `browser-extension-v` 开头的最新版本。
- 这些扩展 Release 是 **Pre-release**，不要用仓库首页的 “Latest” 按钮判断浏览器扩展版本——`Latest` 当前可能指向微信视频号取件扩展。
- 解压 ZIP 后，在 Chrome/Edge 扩展页开启开发者模式，选择「加载已解压的扩展程序」，指向解压后的文件夹。
- Chrome Web Store / Edge Add-ons 版本上架后，会在这里更新说明。

## 微信视频号取件

这是 Amber 的可选扩展，独立于浏览器扩展发布：

- 进入 Releases，选择标签以 `weixin-channels-v` 开头的最新版本。
- 每个平台分别下载 `amber-wx-<platform>.zip` 和对应的 `.sha256`。
- 应用内「设置 → 扩展 → 从 GitHub 安装」会读取同一个渠道的资产。

## 隐私

Amber 下载助手只与本机 `127.0.0.1:31733` 上的 Amber 通信，不向开发者或外部服务器上传数据，不读取 Cookie、登录态或请求头。

完整说明见 [PRIVACY.md](PRIVACY.md)。

## 支持

安装、常见问题和错误反馈见 [SUPPORT.md](SUPPORT.md)。

需要进一步帮助时，请在 [Issues](https://github.com/sumi856/Amber/issues) 提交问题，并附上扩展版本、浏览器版本和操作步骤。请勿发送 Cookie、登录凭据或请求头。

## 说明

本仓库只存放发布资产和面向用户的说明文档，不存放 Amber 应用源码。
