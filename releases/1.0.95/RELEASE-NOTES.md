# MFL Android 1.0.95

## 本地联机
- `read: message too long` / `use of closed network connection` 等连接被关闭类错误，
  现在会**自动用新连接重拨一次**（300ms 后），不再一次失败就退出。
- UDP 读缓冲已按 64KB 收取（MTU 载荷 1464 会导致整包被丢）。

## 版本
- versionName 1.0.95 / versionCode 96
