# MFL Android 1.0.105

## HRS 登录（修复「点使用 HRS 直接已取消」）
- 根因：HRS 这个 client **不允许请求 `profile`/`email`/`hrs.qq`/`hrs.avatar`**，
  授权端点直接 303 回 `error=invalid_scope`（实测原文：
  "The OAuth 2.0 Client is not allowed to request scope 'profile'"）。
- scope 已回退为唯一被允许的一组：`openid offline_access hrs.entitlement`。

## 更新下载
- 前台服务新增 `PARTIAL_WAKE_LOCK`：锁屏/切后台时 CPU 不休眠，下载继续；
- `START_STICKY` + `stopWithTask="false"`：服务被杀后会被拉起，配合断点续传；
- 服务生命周期写入 `externalCacheDir/updates/service.log`，便于定位「服务到底起没起」。

## 版本
- versionName 1.0.105 / versionCode 106
