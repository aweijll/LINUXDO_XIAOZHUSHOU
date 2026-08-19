# 下载与校验

## 官方下载位置

只从以下页面下载：

`https://github.com/aweijll/LINUXDO_XIAOZHUSHOU/releases`

APK 不会提交到 Git 仓库历史，而是作为每个版本的 Release 附件发布。

## Windows 校验 SHA-256

```powershell
Get-FileHash -LiteralPath '.\LINUXDO_XIAOZHUSHOU-v0.32.49.apk' -Algorithm SHA256
```

## Android 校验

可使用支持 SHA-256 的文件管理器或校验工具，将结果与 Release 页面公布值逐字比较。

## 当前版本

- 文件：`LINUXDO_XIAOZHUSHOU-v0.32.49.apk`
- 版本：`0.32.49 (195)`
- 大小：`15,240,409` 字节（约 14.53 MiB）
- APK SHA-256：`9150ACFAB7C227A748430FD8F8D3E2887E46C5C30F3729542E25C0A02E194678`
- 签名证书 SHA-256：`0719EFD57FA6103351BBF645EE57D685BE0FD7F4265D17F0EE608C3E1C12F07D`

后续更新应继续使用同一应用签名。若包名、SHA-256、签名或来源不符，请不要安装。
