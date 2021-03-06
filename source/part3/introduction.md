## Niubility概要设计



我们做了什么：
一个微信公众号，提供查书方面的服务  
一个网站，管理用户，抓取数据
利用了第三方API和公开数据

### 消息流图

![](http://7xjfyz.com1.z0.glb.clouddn.com/6_system.png)


### 微信公众号

前端：
前端微信公众号交互窗口

后端：
sae python应用部署应答逻辑  

- 微信框架的选择werobot vs wechat-sdk
- 微信应答流程的设计
- 如何创建角色及kvdb的设计
- sae支持web和wechat

DB:
kvdb存储用户角色数据，以公众号为key
kvdb存储第三方抓取到的统计分析数据


## 管理员网站
前端：
web页面入口

- web端，以豆瓣授权的方式登陆网站并创建用户数据
- AngularJS 与 python

后端：
sae python应用处理网页请求

DB：
kvdb存储网络管理员的登录信息，目前以豆瓣uid为key，存储相关授权信息。


## 第三方接口
豆瓣api OAuth 2.0授权验证 

- douban-sdk的使用
  + OAuth 2.0  
  研究douban api，如何把豆瓣用户和微信用户关联起来，state参数
  + 想读的增加
  douban sdk居然没有封装想读
  想读的post,put接口该怎么用，已经收藏的书该怎么办。  

TED网页抓取

- bs4网页的抓取

## 项目文档链接
https://github.com/csufuyi/niubility/wiki


## 参考问题

- 怎么回复微信的消息？
- 这些回复的流程有无组件可用？

- 怎么拉取豆瓣的消息？
- 拉取豆瓣的消息有无可用组件？

- 如何智慧的应答？
- 记录玩家的状态

- 微信用户？豆瓣用户？以谁为主。

- 如何回复一个好看的HTM5网页








