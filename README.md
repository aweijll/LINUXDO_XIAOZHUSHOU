# 公益小助手

面向 Android 的公益 API 站点聚合管理工具，用一个 APP 集中处理站点登录、签到、数据同步、API Key、模型测试、模型聊天、LINUX.DO 浏览与网页朗读。

> 本仓库只提供官方 APK、使用文档和版本记录，不包含源代码。公开仓库不代表开源，未授予反编译、二次分发或修改应用的许可。

公益小助手不是 LINUX.DO 官方客户端，也不提供 API 中转服务、模型额度、站点账号或注册码。使用者需要自行拥有合法账号和凭据。

## 下载

- 最新版本：[GitHub Releases](https://github.com/aweijll/LINUXDO_XIAOZHUSHOU/releases/latest)
- 当前版本：`0.32.63 (209)`
- 系统要求：Android 8.0（API 26）及以上
- 包名：`com.jxbp.aihub`

请只从本仓库的 Releases 下载，并核对发布页给出的 SHA-256。更新时直接覆盖安装，不要先卸载，否则本机站点、Cookie、API Key、模型和设置可能被删除。

## 主要功能

- 多站点管理：支持 NEWAPI、One API、SUB2API 和自定义站点，集中查看登录、余额、用量、公告、令牌与模型状态。
- 自动任务：支持站内签到、站外签到、数据同步、登录检查、线路检查及焚绝任务报告。
- AI 分析报告：智能、简洁、深度三种模式，支持 Markdown、主帖证据分析和报告朗读。
- 令牌与模型：本地加密保存多个 API Key，支持分组、搜索、多协议测试和不可用模型清理；拉取模型时按 OpenAI、Codex、Claude 三种协议自动轮换，兼容只支持其中某一种的站点。
- 模型聊天：流式回复、历史会话、语音输入、回复朗读和模型候场助手。
- LINUX.DO 工具：内置浏览器、插件中心、正文/回复朗读、快捷导航、公益榜、白嫖达人榜和抢注助手。
- 数据工具：二维码添加、导入导出、WebDAV 加密备份与恢复。
- 个性化：深浅主题、完整悠哉字体、桌面图标、代理和批量并发设置。

## 快速开始

1. 从 [Releases](https://github.com/aweijll/LINUXDO_XIAOZHUSHOU/releases/latest) 下载 APK。
2. 在系统设置中允许当前浏览器或文件管理器“安装未知应用”，完成安装。
3. 首次启动保持联网，按 APP 提示完成身份确认和注册码激活；实际激活要求以服务端当前策略为准。
4. 进入“站点”添加站点网址，在内置浏览器完成登录并保存。
5. 先执行一次“同步数据”，确认登录、余额和站点类型正确。
6. 需要模型功能时，在站点详情的令牌管理中配置独立 API 地址和 API Key，再拉取和测试模型。

完整步骤见 [使用说明](docs/USER_GUIDE.md)。

## 权限与隐私

- 相机只用于用户主动扫码；麦克风只用于模型聊天的按住说话。
- 通知、前台服务、唤醒锁和电池优化豁免用于用户主动开启的候场、朗读及后台任务。
- 安装权限只用于下载更新后调起 Android 系统安装确认，不会静默安装。
- 站点 Cookie、API Key、激活令牌和 WebDAV 配置使用 Android Keystore 加密保存在本机。
- WebDAV 数据包在上传前使用独立密码加密；普通站点导出不包含 Cookie、令牌或 API Key。
- AI 报告会把脱敏后的任务内容发送到用户选择的模型线路，请自行评估第三方模型服务的隐私政策。

详细说明见 [隐私、安全与权限](docs/PRIVACY_AND_PERMISSIONS.md)。

## 重要限制

- APP 不会绕过验证码、Cloudflare、Turnstile 或站点安全规则。
- 第三方站点的接口、限流和维护状态可能变化，无法保证永久兼容。
- 后台运行受不同手机厂商省电策略影响，授权后仍不能承诺绝对不被系统终止。
- 自定义 HTTP 站点存在明文传输风险，涉及 Cookie 或 API Key 时应优先使用 HTTPS。
- 使用者应只管理自己有权访问的账户，并遵守 LINUX.DO、站点服务条款及当地法律法规。

## 文档

- [完整使用说明](docs/USER_GUIDE.md)
- [隐私、安全与权限](docs/PRIVACY_AND_PERMISSIONS.md)
- [下载校验说明](docs/VERIFY_DOWNLOAD.md)
- [版本记录](CHANGELOG.md)

## 问题反馈

在 [Issues](https://github.com/aweijll/LINUXDO_XIAOZHUSHOU/issues) 中提供 APP 版本、Android 版本、站点类型、复现步骤和脱敏错误信息。

不要提交 Cookie、API Key、Token、注册码、密码，或包含这些内容的日志和截图。
