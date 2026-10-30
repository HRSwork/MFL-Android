# MFL Android 1.0.106

## 网易 1.21.130 / 协议 898
- 从 PRISM 1.1.0-beta.17 的 `libprism.so` 中确认：
  ```
  mov x0, #0x382   ; 898
  ...              ; 写入 CurrentProtocol
  "1.21.130"
  ```
  （旧分支是 `mov x0, #0x35c` = 860 + `"1.21.120"`，由 `use_new_protocol` 开关切换。）
- 三处一起改：
  - `mflcore/game_protocol.go`：`netEaseProtocolID=898`、`netEaseVersion="1.21.130"`
  - `server-next/internal/platform/main.go`：`protocol.CurrentProtocol=898`、`CurrentVersion="1.21.130"`（两处）
  - `g79client` 大厅搜索/按资源查房：`"version": "1.21.130"`
- 单测改为跟随常量（`netEaseProtocolID` / `netEaseVersion`），以后升级不用再改测试。

## 版本
- versionName 1.0.106 / versionCode 107
