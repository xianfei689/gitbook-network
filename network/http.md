# HTTP



### http协议

#### http

* http 请求与响应

  * request，请求

  > key的一般大写开头，也可以小写，一把大写，基本随开发者喜好。

  * 请求头 header

```json
{
  'Accept':'text/plain,text/html',/*指定客户端能够接受的内容类型，也可以是星号  */
  'Accept-Encoding':'gzip, deflate, br',/*指定浏览器可以支持的web服务器返回内容压缩编码类型。*/
  'Accept-Language':'en,zh',/*语言*/
  'Authorization':'Basic xxxx',/*HTTP授权的证书*/
  'Cache-control':'no-cache',/*指定请求和响应遵从的缓存机制*/ 
  'Content-Type':'text/html',
  'Connection':'close',/*是否是持久链接，http1.1默认持久:Keep-Alive*/
  'Content-Length':233,
  'Date':'Tue, 18 Sep 2018 11:05:26 GMT',
  'access-control-allow-origin':'*',/*允许所有域名的脚本访问该资源,保护静态资源么*/
  'Status':200,
  'Cookie':'xx'
  'Host':'www.baidu.com',
  'User-Agent':'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/69.0.3497.92 Safari/537.36'/*浏览器特征编码*/


}
```

```text
- 请求体
```

* response，响应
  * 响应头 header

```json
{
  'Age':12,//原始服务器到代理缓存形成的估算时间
  'Content-Type':'text/html;charts=utf-8',
  'Cache-Control':'no-cache',/*告诉素有的缓存机制是否可以缓存以及哪种类型*/
  'Content-Languge':'en,zh',
  'Content-Length':2121,/*响应体的长度*/
  'Date':'Tue, 18 Sep 2018 11:05:26 GMT',
  'Expires':'Thu, 01 Dec 2010 16:00:00 GMT'/*响应过期的时间*/,
  'Last-modified':'Thu, 01 Dec 2010 16:00:00 GMT',/*请求资源的最后修改时间*/
  'Server':'IIS/Nginx/Tengine',
  'Set-cookie':'xxxxx设置Cookie'
}
```



1. get和post的区别

   | 操作 | get | post |
   | :--- | :--- | :--- |
   | 后退/刷新 | 无害 | 重复提交 |
   | 编码类型 | application/x-www-form-urlencoded | application/x-www-form-urlencoded/multipart/form-data/二进制 |
   | 历史 | 参数保留在浏览器history里 | 参数不会保留 |
   | 数据类型限制 | ASCII字符 | 没有限制 |
   | 安全性 | 与post相比，比较差，敏感信息不要用get | post比get安全，参数不保留的缘故，在客户端和服务端 |
   | 可见性 | 所有人在url可见 | 在url中不可见 |

2. put 和post 的区别

   | 操作 | put | post |
   | :--- | :--- | :--- |
   | 特性 | 幂等 | 非幂等 |
   | 场景 | 更新资源，修改密码（因为提交参数不同，但结果一样，重复结果，多次不同请求的场景） | 注册账号 |



