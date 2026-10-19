# Amber 下载助手隐私政策

**生效日期：2026-10-20**
**适用范围：Amber 下载助手浏览器扩展（Chrome / Edge / Firefox），以及它与本机 Amber 桌面应用的通信。**

## 摘要

Amber 浏览器扩展不向开发者、广告商、数据分析服务或任何外部服务器发送数据。它只与本机运行的 Amber 桌面应用通信，地址限定为 `http://127.0.0.1:31733`。扩展不读取、保存或传输 Cookie、登录态、认证信息或请求头，也不出售、出租或共享用户数据。

## 扩展处理的数据

1. **页面地址与标题**：当用户点击悬浮条、右键菜单或扩展面板中的交接入口时，扩展把当前页面 URL、页面标题和（如可识别）作品页 URL 交给本机 Amber，用于解析和下载。
2. **媒体地址与基本响应信息**：仅在用户主动启用「更多画质」并授予可选权限后，扩展观察当前页面的媒体响应，取得媒体 URL、内容类型和响应大小，用于列出可选媒体/画质。`webRequest` 观察不读取响应正文；页面脚本只对 `.m3u8` / `.mpd` 清单读取最多 512KB 文本以解析画质/变体，不读取其他响应正文。扩展不读取 Cookie、请求头或登录态，也不拦截或修改请求。
3. **本地设置**：按钮外观、面板主题、待处理交接状态（标题、URL、时间，最长保留 10 分钟）保存在浏览器本地存储中。
4. **任务状态**：扩展从本机 Amber 读取最近任务的状态、进度和标题，用于扩展面板回显；这些数据由本机 Amber 产生并保存在用户设备上。

上述数据只在本机处理。扩展不会把它们上传到开发者或第三方服务器。

## 权限用途

- **全站内容脚本（http/https）**：在视频页面识别 `<video>` 并在视频旁显示交接入口。
- **本机网关 host 权限（127.0.0.1:31733）**：与本机 Amber 通信的唯一通道。
- **`webRequest` + 全站 host（可选）**：只有用户在扩展面板设置里主动启用「更多画质」后才会请求；用于观察媒体响应 URL、类型和大小。不读取请求头、Cookie 或响应正文。
- **`tabs`**：识别当前标签页、发送扩展消息和显示角标。
- **`storage`**：保存按钮外观、面板主题和待处理交接状态。
- **`contextMenus`**：提供页面、链接和视频的右键交接入口。

## 数据共享与用途限制

- 不向任何第三方出售、出租、共享或转让用户数据。
- 不将数据用于广告、用户画像、信用评估、保险或贷款等用途。
- 不运行远程代码，不使用分析 SDK；扩展代码随扩展包一起分发。
- 扩展的唯一用途是帮助用户把当前视频页面交给本机 Amber 处理。

## 保存期限与用户控制

- 待处理交接状态最长保留 10 分钟，或在对应下载任务出现后删除。
- 按钮外观和面板主题一直保存在浏览器扩展存储中，直到用户修改、清除扩展数据或卸载扩展。
- 媒体候选保存在浏览器会话存储/内存中，通常随标签页或浏览器关闭清除；不支持会话存储的浏览器会退化到本地存储，但同样不会上传。
- 下载任务、历史记录和文件由本机 Amber 桌面应用管理，用户可在应用中删除；扩展不保存这些文件的副本。
- 用户可以随时：
  - 在浏览器扩展页停用或卸载扩展；
  - 在扩展详情页撤销站点访问或可选权限；
  - 关闭扩展面板中的「更多画质」；
  - 清除扩展的本地数据；
  - 在 Amber 应用中删除下载记录和本地文件。

## 安全边界

本机网关只监听 `127.0.0.1`，并校验扩展 Origin；扩展不提供远程管理、远程代码执行或云端账户功能。浏览器扩展与 Amber 应用之间的数据不会离开用户设备。

## 儿童

本扩展不面向 13 岁以下儿童，也不会有意收集儿童的个人信息。

## 政策更新

如果本政策发生实质性变化，会更新顶部生效日期，并在发布仓库中提供最新版本。继续使用扩展即表示接受更新后的政策。

## Chrome Web Store 数据使用对照

- **网络记录（Web history）**：扩展处理当前页面 URL、页面标题和媒体请求 URL；仅在本机内存/会话中使用，不上传。
- **网站内容（Website content）**：扩展读取页面中的 `<video>` 元素、页面标题，以及用户启用「更多画质」后命中的 `.m3u8` / `.mpd` 清单文本；仅在本机解析，不上传。
- 不处理个人身份、健康、财务、身份验证、个人通讯或位置数据；不记录点击、鼠标位置、滚动或键盘操作历史。

## 联系方式

如对本政策有疑问，请在本项目的公开资产仓提交 Issue：

https://github.com/sumi856/Amber/issues

---

# Amber Download Assistant Privacy Policy

**Effective date: 2026-10-20**
**Scope: Amber Download Assistant browser extension (Chrome / Edge / Firefox) and its communication with the local Amber desktop application.**

## Summary

The Amber browser extension does not send data to the developer, advertisers, analytics services, or any external server. It communicates only with the Amber desktop application running on the same device at `http://127.0.0.1:31733`. The extension does not read, store, or transmit cookies, login state, credentials, or request headers, and it does not sell, rent, or share user data.

## Data processed by the extension

1. **Page URL and title**: when the user clicks the floating bar, a context menu, or the extension-panel handoff entry, the extension sends the current page URL, page title, and (when identifiable) the work-page URL to the local Amber app for parsing and downloading.
2. **Media URLs and basic response metadata**: only after the user explicitly enables “More qualities” and grants the optional permissions, the extension observes media responses on the current page and records the media URL, content type, and response size to list available media/qualities. `webRequest` observation does not read response bodies; the page script reads only `.m3u8` / `.mpd` manifest text (up to 512 KB) to parse quality variants, and does not read other response bodies. It does not read cookies, request headers, or login state, and it does not block or modify requests.
3. **Local settings**: bar appearance, panel theme, and pending handoff status (title, URL, timestamp; retained for up to 10 minutes) are stored in browser local storage.
4. **Task status**: the extension reads recent task state, progress, and titles from the local Amber app for display in the extension panel. This data is produced and stored locally by Amber.

All processing stays on the user's device. The extension does not upload this data to the developer or any third-party server.

## Permissions

- **Content scripts on http/https sites**: detect `<video>` elements and show the handoff entry next to the video.
- **Local gateway host permission (127.0.0.1:31733)**: the only channel used to communicate with the local Amber app.
- **`webRequest` + all-site host permission (optional)**: requested only when the user enables “More qualities” in the extension panel. Used to observe media response URLs, types, and sizes. Request headers, cookies, and response bodies are not read.
- **`tabs`**: identify the active tab, send extension messages, and display the badge.
- **`storage`**: save bar appearance, panel theme, and pending handoff state.
- **`contextMenus`**: provide right-click handoff entries for pages, links, and videos.

## Data sharing and limited use

- No user data is sold, rented, shared, or transferred to third parties.
- Data is not used for advertising, profiling, credit, insurance, or lending purposes.
- No remote code or analytics SDKs are used; the extension code is distributed with the extension package.
- The extension's single purpose is to hand the current video page to the local Amber application.

## Retention and user controls

- Pending handoff state is retained for at most 10 minutes or until the corresponding download task appears.
- Bar appearance and panel theme remain in extension storage until the user changes them, clears extension data, or uninstalls the extension.
- Media candidates remain in browser session storage/memory and are normally cleared when the tab or browser closes. Browsers without session storage fall back to local storage; they are still not uploaded.
- Download tasks, history, and files are managed by the local Amber desktop application and can be deleted there; the extension does not keep copies of those files.
- Users can at any time disable or uninstall the extension, revoke site access or optional permissions from the browser's extension settings, turn off “More qualities” in the extension panel, clear extension data, or delete download history and local files in Amber.

## Security boundaries

The local gateway binds only to `127.0.0.1` and validates extension origins. The extension provides no remote administration, remote code execution, or cloud account features. Data exchanged between the extension and Amber does not leave the user's device.

## Children

The extension is not directed to children under 13 and does not knowingly collect personal information from children.

## Changes

If this policy changes materially, the effective date above will be updated and the latest version will remain available in the public repository.

## Chrome Web Store data-use mapping

- **Web history**: the extension handles the current page URL, page title, and media request URLs; this stays in local memory/session storage and is not uploaded.
- **Website content**: the extension reads `<video>` elements, page title, and (when More qualities is enabled) `.m3u8` / `.mpd` manifest text; parsing stays local and is not uploaded.
- It does not handle personally identifying, health, financial, authentication, personal communications, or location data, and does not record click, pointer, scroll, or keyboard activity history.

## Contact

For privacy questions, open an issue in the public assets repository:

https://github.com/sumi856/Amber/issues
