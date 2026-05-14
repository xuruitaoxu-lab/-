# 常见问题排查

## 1. 手机显示 net::ERR_CONNECTION_CLOSED

原因通常不是网页代码坏了，而是公网隧道断开或网络拦截。

解决：

```powershell
heart-stop
heart-local
cloudflared tunnel --protocol http2 --url http://127.0.0.1:8790
```

重新复制新生成的 `https://xxxx.trycloudflare.com` 链接到手机打开。

## 2. Cloudflare Tunnel 打开不了

检查：

- PowerShell 窗口是否还开着。
- 日志里是否出现 `Registered tunnel connection`。
- 电脑是否有网络。
- 是否用了新的 trycloudflare 链接。
- 手机 VPN 或代理是否影响访问。

## 3. 摄像头打不开

可能原因：

- 浏览器没有摄像头权限。
- 页面不是 HTTPS。
- 手机浏览器限制摄像头 API。
- 摄像头被其他软件占用。

解决：

- 点击“启动摄像头”。
- 检查浏览器权限设置。
- 关闭占用摄像头的软件。
- 换 Edge、Chrome、QQ 或微信内置浏览器。

## 4. QQ / 微信能打开，外部浏览器打不开

可能是外部浏览器对 WebGL、ES Module、CDN 或 HTTPS 权限处理不同。

建议：

- 使用 Cloudflare Tunnel 的 HTTP2 模式。
- 关闭手机 VPN/代理。
- 尝试 Edge、Chrome、QQ、微信内置浏览器。
- 降低粒子数量。

## 5. 手机百度浏览器很卡

百度浏览器对 WebGL 和摄像头实时识别支持较弱。

建议：

- 使用低负载模式。
- 减少粒子数量。
- 关闭其他后台应用。
- 尽量换 Edge、Chrome、QQ 或微信。

## 6. 菜单不显示

可能原因：

- 浏览器阻止了外部模块。
- 页面被旧缓存覆盖。
- 某些手机浏览器对菜单库兼容不好。

解决：

- 强制刷新页面。
- 换一个新生成的 Cloudflare 链接。
- 清理浏览器缓存。
- 使用原生 HTML 菜单，不依赖外部 GUI 库。

## 7. 页面加载一下就崩溃

通常是手机浏览器 WebGL 内存不足或粒子数过高。

解决：

- 降低粒子数量。
- 降低 `renderer.setPixelRatio`。
- 关闭抗锯齿。
- 关闭摄像头预览或降低摄像头分辨率。
- 使用性能更好的浏览器。

## 8. GitHub 上传后发现密钥泄露

如果误传了 token/API Key：

1. 立刻去对应平台删除或重置密钥。
2. 从仓库历史中清理密钥。
3. 不要只删除当前文件，因为 Git 历史里仍可能存在。