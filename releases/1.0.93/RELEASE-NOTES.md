# MFL Android 1.0.93

## NBT 导入
- 原版「紫色平台」= `minecraft:magenta_stained_glass`（品红色染色玻璃）11×11 地板。
- 修复：创建 NBT 操作台**之前**先无条件铺平台；`structure delete` 探针连续 3 次超时后
  不再死等，直接铺地板继续导入（此前探针不回 → 30 秒超时 → 平台永远不出现）。

## 版本
- versionName 1.0.93 / versionCode 94
