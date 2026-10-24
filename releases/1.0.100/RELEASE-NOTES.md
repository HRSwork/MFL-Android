# MFL Android 1.0.100

## 社区聊天图片
- 聊天里的图片现在会**真正渲染**（此前只显示一个「图片」角标）。
- 服务端新增 `GET /api/chat/images/<id>?format=json`（返回 data URL），
  客户端通过加密网关取回并解码成 Bitmap。
- 取不到时显示「图片加载失败」，不再是一片空白。

## 服务端
- 已部署：binary `4ea4ee5ed00370ba…`，路由 `/api/chat/images/*` 支持 `format=json`。

## 版本
- versionName 1.0.100 / versionCode 101
