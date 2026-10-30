# MFL Android 1.0.110

## 网易 1.21.130：进世界后被本地关闭的修复
- `packet.go`：PyRpc（ModEventS2C / SyncModAttrs）解码失败不再 `panic`，改为记录并跳过该帧；
- 之前表现为「进入世界 1~3 秒后断开」，Disconnect 原因为空，只留下 `use of closed network connection`。

## 版本
- versionName 1.0.110 / versionCode 111
