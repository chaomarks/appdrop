# 闪装 AppDrop

闪装 AppDrop 是一个自托管的 Android APK 分发与管理工具，包含服务端 Web 管理后台和 Android 客户端。你可以用它创建仓库、上传 APK、管理应用图标和版本，并在手机/电视端浏览和下载安装。
<img width="1912" height="861" alt="image" src="https://github.com/user-attachments/assets/88a57b0e-1b96-4698-8901-96b322e4c044" />


## Docker 镜像

DockerHub：<https://hub.docker.com/r/mark8857857/appdrop>

```bash
docker run -d \
  --name appdrop \
  -p 8858:8858 \
  -v /your/data/path:/data \
  mark8857857/appdrop:latest
```

指定 1.6 版本：

```bash
docker run -d \
  --name appdrop \
  -p 8858:8858 \
  -v /your/data/path:/data \
  mark8857857/appdrop:1.6
```

默认访问地址：

```text
http://你的服务器IP:8858
```

## Android 客户端

当前版本：1.6.0

下载 APK：

- [闪装1.6.0.apk](https://github.com/chaomarks/appdrop/releases/tag/v1.6.0)

## 1.6.0 更新内容

- 手机端仓库首页按系统返回键时增加退出确认弹窗，避免误触后直接回到桌面。
- 修复重新打开客户端后仓库首页连接失败时缺少恢复入口的问题。
- 仓库首页连接失败时增加“重试”和“重新登录”操作。
- 登录状态失效时自动清理本地 token，并跳转回登录页。
- 服务端右上角增加 GitHub 和 DockerHub 快捷入口。
- 服务端版本升级到 1.6。
- 内置客户端 APK 同步为 1.6.0。

## 镜像架构

- `mark8857857/appdrop:1.6`：linux/amd64
- `mark8857857/appdrop:latest`：linux/amd64、linux/arm64
