# 下载与校验

## 官方下载位置

只从官方 GitHub Releases 下载：

- [最新 Release](https://github.com/aweijll/LINUXDO_XIAOZHUSHOU/releases/latest)
- [全部 Release](https://github.com/aweijll/LINUXDO_XIAOZHUSHOU/releases)

当前仓库只提供官方 APK、文档和版本记录，不在 Git 历史中提交 APK 源文件。

## 当前版本：0.32.150

- 文件：`LINUXDO_XIAOZHUSHOU-v0.32.150.apk`
- versionCode：`296`
- 大小：`61,994,709 bytes`（约 `59.12 MiB`）
- APK SHA-256：`355536e0eccc13aac5b67c454658d7ce41dfc5eefa75ba9a7e2a6827312ece69`
- 签名证书 SHA-256：`0719efd57fa6103351bbf645ee57d685be0fd7f4265d17f0ee608c3e1c12f07d`
- 包名：`com.jxbp.aihub`
- 架构：仅 `arm64-v8a`；22 个原生库通过 16 KiB 对齐检查
- 系统要求：Android 8.0（API 26）及以上

本页记录对应 0.32.150；未来版本请同时核对相应 Release，不能用旧版哈希校验新版 APK。

## Windows PowerShell

```powershell
Get-FileHash -LiteralPath '.\LINUXDO_XIAOZHUSHOU-v0.32.150.apk' -Algorithm SHA256
```

大小必须为 `61994709` 字节，SHA-256 必须完全一致。

## Linux / macOS

```bash
sha256sum LINUXDO_XIAOZHUSHOU-v0.32.150.apk
# 或
shasum -a 256 LINUXDO_XIAOZHUSHOU-v0.32.150.apk
```

## 安装前检查

以下任意一项不匹配，都不要安装：

- 地址不是 `github.com/aweijll/LINUXDO_XIAOZHUSHOU`；
- 文件名、版本号或大小不对；
- SHA-256 不一致；
- 签名证书不是本页记录的官方证书；
- APK 来自聊天群、网盘、私聊链接或不明镜像。

更新时直接覆盖安装，不要先卸载。卸载会删除 APP 私有数据。
