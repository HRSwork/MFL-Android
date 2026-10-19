# MFL Android 1.0.87

## 聊天页修复
- **自己的消息回到右边**：上一版为修"头像被挤扁"把 Row 改成 weight 布局时，
  把 `horizontalArrangement` 一起丢了（默认 Start），于是自己的消息跑到左边。
  现在用 `Arrangement.End/Start` 恢复左右分边，同时保留"头像固定 34dp 不被压扁"。
- **键盘弹出时聊天记录跟手上移**：edge-to-edge 下 `adjustResize` 不会自动 resize，
  只靠 `imePadding()` 是"输入框上去了、列表没跟上"。现在监听 IME 高度变化，
  键盘弹起时把列表滚到最新一条。

## 版本
- versionName 1.0.87 / versionCode 88
