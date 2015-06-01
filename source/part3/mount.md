我们的python后端既要支持微信的web接口，又要支持管理员登陆的web接口。如何实现？


简单的想法是，一个bottle支持不同的消息路由的目录。

可是我们使用了werobot框架，它已经将bottle封装起来了，很难去复用它来支持web接口。


mount出现了

补充mount介绍。

mount能让父bottle挂载子bottle，子bottle处理微信的请求，父bottle处理web请求。
不同的功能分开处理。