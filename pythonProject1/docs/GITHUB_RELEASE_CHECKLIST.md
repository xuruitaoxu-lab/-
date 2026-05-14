# GitHub 发布清单

## 建议上传的文件

```text
index.html
README.md
docs/USAGE.md
docs/DEPLOYMENT.md
docs/TROUBLESHOOTING.md
docs/PROJECT_SUMMARY.md
```

## 不建议上传的文件

```text
.idea/
.venv/
index.html.bak-*
*.log
.env
任何包含 token、API Key、Authtoken 的文件
```

## 推荐仓库描述

```text
Gesture-controlled 3D particle heart built with Three.js and MediaPipe Hands.
```

## 推荐 Topics

```text
threejs, webgl, mediapipe, hand-tracking, gesture-control, particle-system, creative-coding, interactive-art, javascript, mobile-web
```

## 上传前检查

- [ ] 页面可以在电脑 Edge / Chrome 打开。
- [ ] README.md 能正常显示图片、表格和链接。
- [ ] docs 目录文件完整。
- [ ] 没有上传 `.venv` 和 `.idea`。
- [ ] 没有上传 ngrok token、Cloudflare token、API Key。
- [ ] 如果使用 Cloudflare Tunnel，文档中说明了临时链接每次会变化。

## 可选 .gitignore

```gitignore
.idea/
.venv/
*.bak*
*.log
.env
```