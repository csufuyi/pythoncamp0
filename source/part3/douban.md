
## 豆瓣

对豆瓣sdk的选择也经历了类似的过程 
 
1. 首先查看豆瓣开发者模式的官方文档，确认基本流程
2. 其次查看网络上关于豆瓣api使用的例子，发现很多人使用的时候是没有OAuth授权的。

+ 这样的好处是，使用简单
+ 缺点是：使用频率有限制；无法使用那些必须使用OAuth授权的接口，比如标记想读。

3. 考虑到我们本身要使用OAuth接口的功能，同时，我们的网站登录也需要采取支持第三方登录的方式来管理用户。所以，我们使用了douban-sdk.

豆瓣sdk居然没有提供想读的接口，我们需要对其做一些扩展，使得豆瓣支持我们的功能。

OAuth2.0


了解原理：
refresh_token 只有在access_toke过期以后才能使用。
且只能使用一次。

douban的OAuth2.0
http://developers.douban.com/wiki/?title=oauth2

douban api封装
https://github.com/douban/douban-client


- saecloud deploy 不能使用代理上网的方式提交，会报svn错误
- oauth 2.0之类的key一定不能填错，否则sae也不会打印任何异常的
- python 安装2.7.9的新版本以后，注意原始的版本要做软链接，不然会有很多奇怪的问题
~
~



