# MFL Android 1.0.102

## 后台更新
- 更新下载改由**前台服务**（`UpdateDownloadService`，foregroundServiceType=dataSync）托管：
  切到后台、锁屏都不会再被系统冻结，下载继续。
- 通知栏保留「正在下载更新」常驻通知，下载完成后自动收起并拉起安装界面。

## 版本
- versionName 1.0.102 / versionCode 103
