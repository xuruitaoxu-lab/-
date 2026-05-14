# 项目分类总结

## 一句话介绍

这是一个支持手势控制的 3D 粒子爱心网页，用户可以通过摄像头用手势控制爱心粒子的聚拢、分散、平移和旋转。

## 项目定位

| 项目维度 | 内容 |
| --- | --- |
| 类型 | 创意互动网页 |
| 技术方向 | WebGL、Three.js、手势识别、前端动画 |
| 展示对象 | 3D 粒子爱心 |
| 交互方式 | 摄像头手势识别 |
| 主要平台 | 电脑浏览器、手机浏览器、QQ/微信内置浏览器 |

## 功能分类

### 1. 粒子视觉效果

- 3D 爱心粒子模型
- 粒子呼吸动画
- 粒子颜色调节
- 粒子大小调节
- 多形状切换

### 2. 手势识别交互

- 手掌张开触发分散
- 手掌收缩触发聚拢
- 左右移动控制平移
- 挥手控制旋转
- 上下动作控制角度变化

### 3. 浏览器兼容

- 电脑 Edge / Chrome 优先支持
- 手机 QQ / 微信内置浏览器可用
- 对百度、夸克等浏览器做低负载兼容
- 使用 HTTPS 隧道支持摄像头权限

### 4. 手机访问

- 支持 Cloudflare Tunnel
- 支持 Ngrok
- 可扩展到 GitHub Pages、Netlify、Vercel 等静态部署平台

## 项目亮点

- 单文件即可运行，易于展示和分享。
- 使用真实摄像头手势，而不是鼠标模拟。
- 粒子爱心具有较强视觉冲击力。
- 可作为 WebGL、Three.js、MediaPipe 的学习案例。
- 支持手机远程访问电脑本地网页。

## 适合写在 GitHub About 里的内容

```text
A gesture-controlled 3D particle heart built with Three.js and MediaPipe Hands. Supports hand tracking, particle dispersion, gathering, movement, rotation, and mobile browser access via Cloudflare Tunnel.
```

## 推荐 GitHub Topics

```text
threejs
webgl
mediapipe
hand-tracking
gesture-control
particle-system
creative-coding
interactive-art
html-css-javascript
mobile-web
```

## 建议仓库名

```text
gesture-particle-heart
```

或者中文名：

```text
手势爱心粒子互动网页
```