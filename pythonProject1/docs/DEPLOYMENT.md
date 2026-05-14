# 部署和手机访问说明

这个项目可以用三种方式运行：本地打开、本机公网中转、静态托管。

## 1. 本地打开

适合只在电脑上演示。

```text
D:\Pycharm\Project\pythonProject1\index.html
```

优点：最简单，不需要额外服务。

缺点：手机不能直接访问，摄像头权限在部分浏览器里可能受限。

## 2. Cloudflare Tunnel 手机访问

适合让手机访问电脑正在运行的项目。

推荐稳定命令：

```powershell
heart-stop
heart-local
cloudflared tunnel --protocol http2 --url http://127.0.0.1:8790
```

终端会打印类似：

```text
https://xxxx.trycloudflare.com
```

手机打开这个链接即可。

### 注意

- PowerShell 窗口必须保持打开。
- 电脑必须联网。
- 免费 quick tunnel 的域名每次重启都会变化。
- 如果校园网或手机网不稳定，优先使用 `--protocol http2`。

## 3. Ngrok 固定域名访问

如果已经配置 ngrok 固定域名，可以用固定链接访问。

优点：链接可以相对固定。

缺点：免费版可能出现浏览器警告页，部分手机浏览器体验不好。

## 4. 静态网站托管

可以上传到 GitHub Pages、Netlify、Vercel 等平台。

优点：不需要电脑一直开机。

缺点：部分 CDN、模块导入、摄像头权限和手机浏览器兼容性需要额外处理。

## 5. 发布到 GitHub 前建议

上传前建议只保留：

```text
index.html
README.md
docs/
```

不建议上传：

```text
.venv/
.idea/
index.html.bak-*
任何 token / API Key / ngrok 配置文件
```

可选 `.gitignore` 内容：

```gitignore
.idea/
.venv/
*.bak*
*.log
.env
```