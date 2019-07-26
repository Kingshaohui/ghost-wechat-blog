## 友情提醒
本小程序后端依赖`ghost`开源博客框架，若没有ghost博客的，可以参考基于云开发的博客小程序「无需后端」，开源地址：[https://github.com/CavinCao/mini-blog](https://github.com/CavinCao/mini-blog)

## 更新记录
#### 2019-04-13更新
1. 评论通知功能实现
2. 已知问题修复

相关文章参考：
- [[博客小程序]评论通知功能实现(一)——小程序发送模板消息的几种实现](https://www.bug2048.com/wechat20190411/)
- [[博客小程序]评论通知功能实现(二)——实战过程中的坑](https://www.bug2048.com/wechat20190413/)

#### 2018-10-15更新

1. 生成海报功能
2. 已知问题修复

相关文章参考：
- [利用云开发优化博客小程序（三）——生成海报功能](https://www.bug2048.com/wechat20181015/)

#### 2018-09-30更新

1. 新增公众号关注组件
2. 评论、点赞功能实现，浏览量统计
3. 已知问题修复

相关文章参考：
- [利用云开发优化博客小程序（一）——浏览量统计](https://www.bug2048.com/wechat20190917/)
- [利用云开发优化博客小程序（二）——评论功能](https://www.bug2048.com/wechat20180930/)

#### 2018-07-05更新

wx.getUserInfo官方文档中做了一些调整,授权方式做了下调整，相关文章参考：
- [微信小程序版博客——授权登录的修改(wx.getUserInfo)](https://www.bug2048.com/wechat20180705/)

--------------------------------------------------------------------------------
> 花了点时间陆陆续续，拼拼凑凑将我的小程序版博客搭建完了，这里做个简单的分享和总结。

## 一些体会

四月份的空余时间都在折腾自己的微信小程序版博客，作为后端开发的我鼓捣起前端的技术还是稍微有点吃力的，有些语法确实不太熟悉。

但总的来说还好，静下心来看看文档，熟悉下语法，实现一些功能的时候还是挺有成就感的。

对于小程序，基础的语法和API调用，我觉得腾讯的官方文档已经写了非常详细了，完全可以通过阅读文档来熟悉小程序。

对于基础还是要花点时间静下心来去学学，毕竟有时候无脑百度也挺花时间的。一些容易遗忘的点还是要做好笔记，相信如果一个月没碰前端的代码，估计也忘的7788了。

前阵子`mpvue`很火，有时间的话也希望自己能体验一把。

## 相关文章

在开发的同时也积累了一些文章，用于记录和分享本次开发小程序的过程：

1. [微信小程序版博客——前期准备](https://www.bug2048.com/wechat20180419/)
2. [微信小程序版博客——整体框架搭建](https://www.bug2048.com/wechat20180421/)
3. [微信小程序版博客——图片相关处理](https://www.bug2048.com/wechat20180424/)
4. [微信小程序版博客——列表页相关问题汇总](https://www.bug2048.com/wechat20180425/)
5. [微信小程序版博客——文章详情页设计及问题汇总](https://www.bug2048.com/wechat20180428/)
6. [微信小程序版博客——小程序授权登陆的一点优化](https://www.bug2048.com/wechat20180429/)
7. [微信小程序版博客——用户中心页面设计问题汇总](https://www.bug2048.com/wechat20180501/)
8. [微信小程序版博客——小优化](https://www.bug2048.com/wechat20180502/)

## 关于审核

小程序审核不是一帆风顺，我审核了三次才通过，主要还是服务类目选择的问题，像博客这种应该选择`教育` > `教育信息服务`这类，这个需要注意下，在5月1日劳动节的时候，终于发布了我的1.0版本：

![image](http://image.bug2048.com/1525220924740.jpg)

## 总结

作为程序员，还是需要有一个地方去记录你的知识积累，毕竟大脑的记忆还是有限的，你需要去不断总结，不断积累，为了更好的沉淀。

相信总有一天，量变总会达到质变。

## 其他

补充下利用小程序云开发的数据库的结构：

- posts_statistics（记录文章的点评，喜欢数量）

```

"_id": W5y6i7orBK9ufeyD
//点评数量
"comment_count": 8
//喜欢数量
"like_count": 14
//文章id
"post_id": 5b3de6b464546644ae0b7eb4
//访问数量
"view_count": 231

```

- posts_comments (文章点评记录表)

```
"_id": W69AgvD0YIt7pc32
"_openid": ''
"cAvatarUrl": ''//头像
"cNickName": ''//昵称
"childComment"://子评论
	[
		{"cAvatarUrl":"","cNickName":"","cOpenId":"","comment":"","createDate":"2018-10-17","flag":0,"tNickName":"","tOpenId":"","timestamp":1539706875589}
	]
"comment": ''
"createDate": 2018-09-29
"flag": 0
"postId": 5ba057e864546644ae0b7ee5
"timestamp": 1538211970612
```

最后贴下自己的小程序二维码：

![image](http://image.bug2048.com/gh_e63f2dcd02ee_258.jpg)


> 博客地址：[http//:www.bug2048.com](https://www.bug2048.com/)  
> 微信公众号与微信：Bug生活2048

![image](https://www.bug2048.com//content/images/2018/02/qrcode_for_gh_cac1ef8c9733_258.jpg)

![image](http://image.bug2048.com/WechatIMG2.jpeg?imageView2/1/w/200/h/200/q/100)

