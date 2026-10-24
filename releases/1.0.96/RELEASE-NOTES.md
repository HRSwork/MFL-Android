# MFL Android 1.0.96

## 本地联机
- 进房失败（含 `Enter room failed due to unknown reason (code = 3)`）现在会**自动重试 5 次、每次间隔 1 秒**，
  与原版 `connectTanLobby`（maxRetries=5）一致；以前一次失败就退出。
- `read: message too long`：UDP 收包按 64KB 收取，不再整包被内核丢弃。

## 发布流程
- 发布脚本现在**同时**写两条通道：版本记录 + 加密更新清单（App 里显示的更新公告）。

## 版本
- versionName 1.0.96 / versionCode 97
