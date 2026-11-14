# 下载与校验

## 官方下载位置

只从官方 GitHub Releases 下载：

- [最新 Release](https://github.com/aweijll/LINUXDO_XIAOZHUSHOU/releases/latest)

- [全部 Release](https://github.com/aweijll/LINUXDO_XIAOZHUSHOU/releases)

当前仓库只提供官方 APK、文档和版本记录，不在 Git 历史中提交 APK 源文件。

## 当前版本：0.32.178

发布日期：2026-11-14

- 文件：`LINUXDO_XIAOZHUSHOU-v0.32.178.apk`

- versionCode：`324`

- 大小：`100,951,337 bytes`（约 `96.27 MiB`）

- APK SHA-256：`d99f1911cfc523f2e465be4fb38a2a12d40c9a5150b5e2c8b4d9e01cb200ce30`

- 签名方案：V2＋V3 验签通过；沿用原证书

- 签名证书 SHA-256：`0719efd57fa6103351bbf645ee57d685be0fd7f4265d17f0ee608c3e1c12f07d`

- 包名：`com.jxbp.aihub`

- 架构：仅 `arm64-v8a`；31 个原生库通过 16 KiB 对齐检查

- 系统要求：Android 8.0（API 26）及以上

本页记录对应 0.32.178；未来版本请同时核对相应 Release，不能用旧版哈希校验新版 APK。

## Windows PowerShell

```powershell

Get-FileHash -LiteralPath '.\LINUXDO_XIAOZHUSHOU-v0.32.178.apk' -Algorithm SHA256

```

大小必须为 `100951337` 字节，SHA-256 必须完全一致。

## Linux / macOS

```bash

sha256sum LINUXDO_XIAOZHUSHOU-v0.32.178.apk

# 或

shasum -a 256 LINUXDO_XIAOZHUSHOU-v0.32.178.apk

```

## 安装前检查

以下任意一项不匹配，都不要安装：

- 地址不是 `github.com/aweijll/LINUXDO_XIAOZHUSHOU`；

- 文件名、版本号或大小不对；

- SHA-256 不一致；

- 签名证书不是本页记录的官方证书；

- APK 来自聊天群、网盘、私聊链接或不明镜像。

更新时直接覆盖安装，不要先卸载。卸载会删除 APP 私有数据。

## 授权验收范围

文件哈希、签名和自动检查不能替代真人登录验收；LinuxDo 登录、本人验证、同意授权和注册码绑定仍需在实际 Android 设备上确认，本次未记录真人账号完成全流程的测试。匿名探测确认主通道及后台回调可达，但官方授权页 GET 返回 403，尚未验证实际 WebView 登录页面兼容性。
