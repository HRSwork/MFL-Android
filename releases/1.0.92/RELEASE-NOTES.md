# MFL Android 1.0.92

## 进房连接
- `use of closed network connection` 时**自动用新连接重试一次**（300ms 后），
  其他错误（版本过旧/超时/房间不存在）不重试，避免无谓等待。

## 建筑导入
- 去掉「全部 / 本机 / 云端」分栏与卡片上的"本机/云端"标签，合并成一个列表；
  标题改为"共 N 个建筑"。

## 版本
- versionName 1.0.92 / versionCode 93
