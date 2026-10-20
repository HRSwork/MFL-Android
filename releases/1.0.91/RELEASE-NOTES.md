# MFL Android 1.0.91

## 自己的消息固定靠右（根因修复）
- 服务端消息视图补 `mine` 字段（此前完全没有，客户端只能拿 user_id 猜）；
- 客户端渲染时用可观察的 `myUserId` 再判一次（profile 晚到也会自动重组）；
- 布局改成 `Spacer(weight)` 明确左右，不再依赖 alignment/weight 的微妙行为。

## 版本
- versionName 1.0.91 / versionCode 92
