# 手势爱心粒子互动网页

一个基于 Three.js 和 MediaPipe Hands 的手势互动粒子爱心网页。页面会把大量粒子组成 3D 爱心，并通过摄像头识别手势，实现聚拢、分散、跟随移动和旋转等效果。

## 项目分类

| 分类 | 说明 |
| --- | --- |
| 项目类型 | 前端单页互动网页 |
| 主要效果 | 3D 粒子爱心、手势控制、粒子聚散、左右/上下跟随、旋转 |
| 运行方式 | 本地浏览器直接运行，或通过本机服务器 + Cloudflare Tunnel/Ngrok 分享到手机 |
| 适用场景 | 创意展示、课堂演示、表白/祝福互动页面、WebGL/手势识别学习项目 |
| 核心文件 | `index.html` |

## 功能特点

- 粒子组成 3D 爱心，并支持动态呼吸效果。
- 手掌张开或靠近画面时，粒子分散。
- 手掌收缩或远离画面时，粒子聚拢。
- 手掌左右移动时，爱心跟随平移。
- 手势挥动时，爱心产生旋转反馈。
- 支持颜色、粒子大小、形状等控制项。
- 针对手机端和弱浏览器做了降负载处理。
- 可通过 Cloudflare Tunnel 或 Ngrok 让手机远程访问电脑上的网页。

## 技术栈

- HTML / CSS / JavaScript
- Three.js：3D 粒子渲染
- MediaPipe Hands：手势识别
- WebGL：浏览器图形加速
- Cloudflare Tunnel / Ngrok：公网访问本地网页

## 目录结构

```text
pythonProject1/
├─ index.html                  # 主页面，包含粒子效果和手势逻辑
├─ README.md                   # GitHub 首页说明
├─ docs/
│  ├─ USAGE.md                 # 使用说明
│  ├─ DEPLOYMENT.md            # 发布和手机访问说明
│  ├─ TROUBLESHOOTING.md       # 常见问题排查
│  └─ PROJECT_SUMMARY.md       # 项目分类总结
└─ index.html.bak-*            # 本地备份文件，不建议上传到 GitHub
```

## 快速开始

### 方式一：电脑本地打开

直接用浏览器打开：

```text
D:\Pycharm\Project\pythonProject1\index.html
```

推荐使用 Edge 或 Chrome。

### 方式二：手机访问电脑上的网页

如果已经配置好了本地命令，在 PowerShell 运行：

```powershell
heart-cloudflare
```

或者使用更稳的 HTTP2 模式：

```powershell
heart-stop
heart-local
cloudflared tunnel --protocol http2 --url http://127.0.0.1:8790
```

等待终端打印 `https://xxxx.trycloudflare.com`，手机打开这个链接即可。

## 浏览器建议

| 浏览器 | 推荐程度 | 说明 |
| --- | --- | --- |
| 电脑 Edge / Chrome | 推荐 | 兼容性和性能最好 |
| 手机 QQ / 微信内置浏览器 | 可用 | 通常能打开，但菜单和摄像头权限可能受限制 |
| 手机百度浏览器 | 不推荐 | WebGL 和摄像头性能较弱，可能卡顿 |
| 夸克浏览器 | 一般 | 部分版本可能隐藏菜单或限制模块加载 |

## 注意事项

- 摄像头功能必须在 HTTPS 或 localhost 环境下才能正常使用。
- Cloudflare Tunnel 的免费临时链接每次重启都会变化。
- PowerShell 窗口关闭后，手机访问链接会失效。
- 不要把 ngrok token、API Key 或其他密钥上传到 GitHub。

## 文档

- [使用说明](docs/USAGE.md)
- [部署和手机访问](docs/DEPLOYMENT.md)
- [常见问题排查](docs/TROUBLESHOOTING.md)
- [项目分类总结](docs/PROJECT_SUMMARY.md)