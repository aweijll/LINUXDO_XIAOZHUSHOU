# 公益小助手

Android 上的多站点管理、模型聊天、本地 API 网关、SSH 工作台、LINUX.DO 浏览和短剧工具。

[![最新版本](https://img.shields.io/github/v/release/aweijll/LINUXDO_XIAOZHUSHOU?label=最新版本)](https://github.com/aweijll/LINUXDO_XIAOZHUSHOU/releases/latest)
[![Android](https://img.shields.io/badge/Android-8.0%2B-3ddc84)](https://github.com/aweijll/LINUXDO_XIAOZHUSHOU/releases/latest)

## 下载与安装

当前稳定版 **0.32.151**，更新日期 **2026-10-07**。Android 8.0（API 26）及以上，**仅支持 ARM64（arm64-v8a）**，安装包 **59.22 MiB**。

- [下载 0.32.151 APK](https://github.com/aweijll/LINUXDO_XIAOZHUSHOU/releases/download/v0.32.151/LINUXDO_XIAOZHUSHOU-v0.32.151.apk)
- [查看最新版本](https://github.com/aweijll/LINUXDO_XIAOZHUSHOU/releases/latest)
- [文件大小、SHA-256 与签名校验](docs/VERIFY_DOWNLOAD.md)

已安装用户可在 APP 内检查更新，或下载 APK 覆盖安装。**不要先卸载旧版本**；换机或重装前先备份。当前不提供 ARM32、x86 或 x86_64 安装包。

## 0.32.151 更新

安装包同时启用 V1、V2、V3，沿用原签名证书；版本号递增以支持从 150 检查更新。功能内容保留 150，安装器兼容效果仍需在受影响手机上确认。

## 0.32.150 功能更新

- **应用公告**：修复无封面公告导致列表和弹窗读取失败的问题。
- **短剧更新**：任务串行排队、分批读取；播放或媒体处理时暂停启动后续更新，减少争抢资源。
- **剧库清理**：显示本地剧目数量和文件占用，支持展开多选站源清理；保留下载视频、追剧及观看记录。
- **站点验证**：修复“在 APP 内验证”无反应，显示准备进度和失败原因，验证后继续原操作。

150 功能基线的 Android 2,389 项单元测试通过、Lint 零错误；151 功能源码未变，重新核验正式构建、三种签名、架构和实际下载一致性。真实站点挑战、播放流畅度和投屏兼容性仍受设备与服务端影响。

## 功能总览

| 模块 | 功能 |
|---|---|
| 站点管理 | NEWAPI、One API、SUB2API、AIHubMix 及兼容站点；账号、Cookie、余额、令牌、标签、收藏、筛选、批量同步与站点代理 |
| 签到与任务 | 自动/手动/站外签到、仅同步、不参与任务；逐站结果、登录恢复及人工验证后的继续处理 |
| 模型中心 | 多站点、多 Key 拉取模型；OpenAI Chat Completions、Responses、Claude Messages 测试；筛选、排序、别名、分组和清理 |
| 模型聊天 | 流式回复、历史会话、语音输入与朗读；模型候场、探测间隔、并发及可用提醒 |
| 本地 API 网关 | 三协议入口、已验证上游协议适配、非流式/SSE、模型路由、优先级、鉴权、回环/局域网监听、持久化日志和用量账本 |
| SSH-AI | 终端、多会话、文件传输、服务器状态、服务与容器管理、端口转发、AI 排障；OpenAI Chat/Responses、Claude、Gemini 协议识别、有界重试、RPM 和并发设置 |
| LINUX.DO | 内置浏览、帖子及回复、通知、排行榜、插件、长帖增量朗读；保留原页面的 APP 内验证流程 |
| 代理与 DoH | HTTP/SOCKS、后台下发及自定义 DoH；独立 ECH、引导 IP、IPv6、TLS/HTTP2 转接、上游代理与 DNS 缓存管理 |
| 短剧 | 多站源、搜索、分类、同系列推荐、追剧、历史、下载、播放与投屏；源配置同步、站点验证、更新队列和缓存清理 |
| 资源与媒体 | 资源分类、视频、直播、听书、媒体通知、锁屏控制和 DLNA 投屏 |
| 公益榜与公告 | 公益站排行榜、站点详情及主帖入口；应用公告列表和后台开启的弹窗通知 |
| 备份与设置 | 配置导入导出、二维码、加密 WebDAV/文件备份、多保险箱、主题、明暗模式、字体、桌面图标、激活与续费 |

完整分类见 [功能地图](docs/FEATURES.md)，操作步骤见 [使用说明](docs/USER_GUIDE.md)。

## 快速开始

1. 安装 APK，联网按授权页提示完成身份确认和激活。
2. 在“站点”添加网址并登录，执行“同步数据”。
3. 配置站点 API 地址和 Key，拉取并测试模型，再进入聊天。
4. 需要对接电脑客户端时开启本地网关，使用网关显示的地址、Key 和模型 ID。
5. 管理服务器时进入首页的 SSH-AI；使用“APP 本地网关”提供方前先开启网关。
6. 短剧从“全部资源”进入；同步源配置后按需更新，遇到真实验证提示时在 APP 内完成。
7. 在设置查看应用公告、检查更新和配置备份。

## 连接与使用边界

- 网关提供 `/v1/models`、`/v1/chat/completions`、`/v1/responses` 和 `/v1/messages`。协议适配不等于支持所有供应商扩展能力；以实际模型测试为准。
- SSH 重试仅用于可安全重试的请求；已输出内容、结果不确定或认证失败时不会盲目重发，SSH 命令不会自动重复执行。
- **短剧固定直连**，不继承 APP 代理、系统静态代理或旧短剧代理配置；系统 VPN、过滤软件和网络环境仍可能影响连接。
- DoH 是加密 DNS/连接路线能力，不是永久免 Cloudflare 验证的保证。403 也可能来自权限、限流或站点规则。
- 源名称、停用和隐藏由后台发布配置控制。源数量和可用性会变化，以 APP 同步后的列表为准。
- 激活、续费、模型和第三方内容均依赖对应服务；套餐价格以 APP 当时展示为准。

## 文档与反馈

- [完整使用说明与常见问题](docs/USER_GUIDE.md)
- [功能地图](docs/FEATURES.md)
- [隐私、安全与权限](docs/PRIVACY_AND_PERMISSIONS.md)
- [下载校验](docs/VERIFY_DOWNLOAD.md)
- [版本记录](CHANGELOG.md)
- [第三方声明](NOTICE.md)

反馈请提供 APP/Android 版本、手机型号、模块、操作步骤和脱敏错误。不要上传 Cookie、API Key、Token、注册码、密码、私钥或备份文件。

## 仓库说明

公益小助手不是 LINUX.DO 官方客户端。本仓库用于发布 APK、文档和版本记录，不包含应用源代码。公开可见不等于开源，也不授予反编译、修改、去授权、二次分发、改包或冒用官方名称的许可。第三方组件和字体按各自许可证执行，详见 [第三方声明](NOTICE.md) 与 `THIRD_PARTY_NOTICES/`。使用站点、模型、服务器和媒体内容时需具备相应访问权限。
