1.自测的时候用QQ和微信自带浏览器都可以正常时候只有在Vivo自带浏览器的时候出现闪退
2.必须要在电脑Powershell上运行heart-stop
heart-local
cloudflared tunnel --protocol http2 --url http://127.0.0.1:8790
3.等它打印新的链接，例如：
https://xxxx.trycloudflare.com
4.手机 QQ/浏览器打开这个新链接。
注意两点：

这个 PowerShell 窗口要一直开着，关了网站就断。
每次重启电脑或重新运行 Cloudflare，trycloudflare.com 链接都会变，要用新打印的链接。
如果你想简化，我建议以后做成一个命令 heart2，你只要输入：

heart2
就自动启动 HTTP2 稳定模式。
