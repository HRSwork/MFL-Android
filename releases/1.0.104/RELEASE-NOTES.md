# MFL Android 1.0.104

## 错误上报（新）
- 出错弹窗直接显示具体错误，并新增「上传错误详情」按钮；
- 服务端 `POST /api/v1/error/report` 按「用户 + 错误指纹」去重：
  第一次返回编号，之后返回 `duplicate: true` 并提示「该问题已上报过，请联系管理团队」。

## HRS 登录
- 回退 1.0.103 之后新增的自定义 scope（hrs.account / hrs.qq / hrs.avatar），
  修复「点使用 HRS 直接显示已取消」（invalid_scope）。

## 版本
- versionName 1.0.104 / versionCode 105
