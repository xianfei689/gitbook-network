# HTTP 协议入门 {#page-title}

---

HTTP 协议是互联网的基础协议，也是网页开发的必备知识，最新版本 HTTP/2 更是让它成为技术热点。

![](/assets/import.png)

HTTP 是基于 TCP/IP 协议的[**应用层协议**](http://www.ruanyifeng.com/blog/2012/05/internet_protocol_suite_part_i.html)。它不涉及数据包（packet）传输，主要规定了**客户端和服务器之间的通信格式**，默认使用80端口。

## 一、HTTP/0.9

HTTP 是基于 TCP/IP 协议的[**应用层协议**](http://www.ruanyifeng.com/blog/2012/05/internet_protocol_suite_part_i.html)。它不涉及数据包（packet）传输，主要规定了客户端和服务器之间的通信格式，默认使用80端口。

最早版本是1991年发布的0.9版。该版本极其简单，只有一个命令`GET`。

> ```js
> GET /index.html
> ```

上面命令表示，TCP 连接（connection）建立后，客户端向服务器请求（request）网页`index.html`。

协议规定，服务器只能回应HTML格式的字符串，不能回应别的格式。

> ```html
> <html>
>   <body>Hello World</body>
> </html>
> ```

服务器发送完毕，就关闭TCP连接。

