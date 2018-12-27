# HTTP



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

