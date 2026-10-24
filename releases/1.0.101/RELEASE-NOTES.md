# MFL Android 1.0.101

## 社区聊天图片（修复「一张都加载不出来」）
- 消息里的 `image` 字段是**完整路径** `/api/chat/images/img-xxx`，
  客户端却把它当成 ID 又拼了一次前缀，请求变成
  `/api/v1/chat/images//api/chat/images/img-xxx` —— 服务端对每一张图都返回 400。
- 现在只取最后一段 ID 再请求；失败时会显示具体原因。

## 版本
- versionName 1.0.101 / versionCode 102
