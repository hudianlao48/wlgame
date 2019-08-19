# 概述

> WeiLi Game APIs是微鲤游戏面向H5游戏开发者提供的基于微鲤游戏内的webView接口。

通过使用WeiLi Game APIs，可以接入微鲤游戏账号系统、调用广告展示等微鲤游戏提供的业务方法，为游戏开发者提供有效的增收手段。

此文档面向H5网页游戏开发者介绍WeiLi Games APIs如何使用及相关注意事项。

# API设计原则

- 微鲤游戏平台本质上是一个webView，我们尽量提供一个标准的浏览器环境，浏览器支持的特性，Weili Game APIs就不再提供了。

	iOS会是WKWebView环境, 官方文档参见 https://developer.apple.com/documentation/webkit/wkwebview

	android会是4.4版本以上基于Chromium的内核。官方文档参见 https://developer.chrome.com/multidevice/webview/overview
- 绝大部分的时候，参数会是一个 JavaScript Object，除非只有一个参数

# 接入步骤

- 首先要在WeiLi Game服务中心申请接入，我们平台会分配一个appid，用于接口的数字签名校验。

- 然后引入wlgamebridge.js，作为内外通信的桥梁。

- 初始化wlgamebridge.js后，就可以调用各种方法控制微鲤游戏的行为了。

# 联系我们
对文档有任何疑问都可以通过以下方式联系我们：

- Email: huhongfei@weli.cn