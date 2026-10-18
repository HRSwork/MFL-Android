# MFL Android（已编译版本）

每个版本的**安装包 + 更新说明 + 校验和**都在本仓库里，同时也在 GitHub Releases 上发布。

## 目录

```
releases/<版本>/
  MFL-<版本>.apk       这个版本的安装包
  RELEASE-NOTES.md     改了什么、怎么验
  SHA256SUMS           校验和
```

## 下载

- 直接在本仓库 `releases/<版本>/MFL-<版本>.apk` 下载；
- 或到 **[Releases](https://github.com/HRSwork/MFL-Android/releases)** 页面下载（最新版标记为 Latest）；
- 更早的版本（1.0.24 ~ 1.0.72）在 Release `android-archive-early` 里。

安装前建议核对 `SHA256SUMS`：

```bash
sha256sum MFL-<版本>.apk
```
