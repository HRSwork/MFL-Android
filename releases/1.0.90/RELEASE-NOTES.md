# MFL Android 1.0.90

## 聊天
- **气泡里不再显示时间戳**（服务端 `at` 字段仍保留，日志 `MFLChat` 里记录 id/at/mine/kind）。
- **QQ 风格圆润气泡**：四角 18dp、贴头像那侧 6dp、1dp 轻阴影、对方气泡加细描边；
  引用块/表情块也改为圆角。
- **键盘弹出聊天记录跟随**：外层 shell 消费了 ime inset，之前读 `WindowInsets.ime`
  一直是 0；改成监听列表可视高度变小 → 滚到最后一条（真正跟手上移）。

## 版本
- versionName 1.0.90 / versionCode 91
