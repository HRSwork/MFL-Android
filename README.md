# MFL Android（已编译版本）

本仓库**不存安装包**：APK 全部作为 **GitHub Releases 资产**发布，每个版本一个 Release。
仓库里只保留这个版本的**更新说明**与**校验和**（`releases/<版本>/`），方便检索与核对。

## 下载

到本仓库 **[Releases](https://github.com/HRSwork/MFL-Android/releases)** 页面：

- 最新版：标记为 **Latest** 的那个 Release
- 历史版本：`v1.0.73` ~ `v1.0.83` 各自一个 Release
- 更早版本（1.0.24 ~ 1.0.72）：统一在 **`android-archive-early`** 这个 Release 里

每个 Release 的资产就是 `MFL-<版本>.apk`；下载后用同目录 `SHA256SUMS` 或 Release 说明里的 sha256 核对。

## 目录约定

```
releases/<版本>/
  RELEASE-NOTES.md     这个版本改了什么、怎么验
  SHA256SUMS           校验和（安装包在 Releases 资产里）
```

> `.gitignore` 明确排除 `*.apk` / `*.aab` / `*.aar` / `*.zip` / `*.jar`：
> 二进制不进 git 历史（之前 11 个 APK 让 `.git` 涨到 253MB，已清理到 216KB）。

## 版本索引

| 版本 | versionCode | 大小 | sha256（前 16 位） | 说明 |
| --- | --- | --- | --- | --- |
| 1.0.83 | 84 | 24,562,680 | `a2d8709cdddc3800` | [说明](releases/1.0.83/RELEASE-NOTES.md) — 资料改为 HRS 管理（不可改名/改头像）、圆形头像、HRS 用户名同步 |
| 1.0.82 | 83 | 24,402,707 | `1e3eaa1f356ead84` | [说明](releases/1.0.82/RELEASE-NOTES.md) — 本地联机假成功修复、断点续传、修补进度、签到日薪 |
| 1.0.81 | 82 | 24,370,035 | `22c9559d8e722a38` | [说明](releases/1.0.81/RELEASE-NOTES.md) — 命令方块/方块实体、data 朝向、铺底边界时机、中继 UDP 缓冲修复 |
| 1.0.80 | 81 | 24,396,259 | `16e58c11824ea98a` | [说明](releases/1.0.80/RELEASE-NOTES.md) — 修复导入朝向与牌子文字；进房失败中文提示与自动退绿宝石 |
| 1.0.79 | 80 | 24,308,779 | `c14f03cdc13ef864` | [说明](releases/1.0.79/RELEASE-NOTES.md) — 下载进度：应用内实时显示百分比与已下载大小，通知栏同步进度条，切后台继续下载 |
| 1.0.78 | 79 | 24,307,203 | `c0ab839802f7c13f` | [说明](releases/1.0.78/RELEASE-NOTES.md) — 内嵌网页登录修复：支持授权页开新窗口与第三方 Cookie，登录完自动回到应用 |
| 1.0.77 | 78 | 24,305,931 | `457cb3798566cd62` | [说明](releases/1.0.77/RELEASE-NOTES.md) — 修复点更新报「Cleartext HTTP traffic not permitted」：安装包改走应用内加密通道（与接口同一套证书校验）下载 |
| 1.0.76 | 77 | 24,226,379 | `b83ebfd204998178` | [说明](releases/1.0.76/RELEASE-NOTES.md) — 应用内静默下载安装更新（含通知栏入口），不再跳浏览器 |
| 1.0.75 | 76 | 24,225,703 | `7d25b0993a074016` | [说明](releases/1.0.75/RELEASE-NOTES.md) — 建筑导入新增三开关：清理周围方块（订阅）、自动铺底层（默认拒绝方块）、自动放边界；自定义材质需订阅 |
| 1.0.74 | 75 | 24,155,355 | `c615e2cdd0719d4d` | [说明](releases/1.0.74/RELEASE-NOTES.md) — .schematic 补齐方块映射：水、岩浆、半砖（含上下位）、各种楼梯、16 色羊毛/地毯/染色玻璃/混凝土、木材家族等 |
| 1.0.73 | 74 | 24,224,675 | `b260366e2a3d7380` | [说明](releases/1.0.73/RELEASE-NOTES.md) — .schematic 补齐方块映射（水/岩浆/半砖/楼梯/染色家族等），此前这些会变成未知方块而丢失 |

> 更早版本（1.0.72 及以前）未归档。

## 安装说明


1. 下载对应版本的 `MFL-<版本>.apk`；
2. 首次安装需要在系统里允许「安装未知应用」（按提示授权一次即可）；
3. 校验：`sha256sum MFL-<版本>.apk` 与 `SHA256SUMS` 一致；
4. 覆盖安装不会清除账号与本地设置。
