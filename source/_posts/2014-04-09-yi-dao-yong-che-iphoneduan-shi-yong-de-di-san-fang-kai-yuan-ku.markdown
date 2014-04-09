---
layout: post
title: "易到用车iPhone端使用的第三方开源库"
date: 2014-04-09 13:25:02 +0800
comments: true
categories: 
---
- [CocoaPods](https://github.com/CocoaPods/CocoaPods) 是一个负责管理iOS项目中第三方开源代码的工具。该项目开始于2011年8月12日，经过一年多的发展，现在已经超过1000次提交，并且持续保持活跃更新。开发iOS项目不可避免地要使用第三方开源库，CocoaPods的出现使得我们可以节省设置和更新第三方开源库的时间。  

- [AFNetworking](https://github.com/AFNetworking/AFNetworking) 是一个轻量级的iOS网络通信类库，继ASI类库不在更新之后开发者们有一套不错选择。  

- [ReactiveCocoa](https://github.com/ReactiveCocoa/ReactiveCocoa) 是github去年开源的一个项目，是在iOS平台上对FRP的实现。FRP的核心是信号，信号在ReactiveCocoa(以下简称RAC)中是通过RACSignal来表示的，信号是数据流，可以被绑定和传递。  

- [EGODatabase](https://github.com/yongche/egodatabase) 是在FMDB基础之上引入了多线程的支持，另EGODatabase提供了异步数据库操作的支持，将数据库操作封装成数据库请求（其继承于NSOperation），数据库请求创建好了，丢到一个OperationQueue中被异步的进行执行，当请求数据完成之后 ，相应的delegate方法会被调用，然后你可以在主线程更新显示了。  

- [MBProgressHUD](https://github.com/jdg/MBProgressHUD) 主要作用为应用显示一个过渡的作用，常用于打开一个联网页面加载过程，防止出现假死现象，如果网速慢则告诉用户已经在很努力很努力的加载中。

- [Reachability](https://github.com/tonymillion/Reachability) 是苹果官方给的检查网络状态的库。  

- [SDWebImage](https://github.com/rs/SDWebImage) 通过对UIImageView的类别扩展来实现异步加载替换图片的工作。  

- [YCVoice](https://github.com/yongche/yc-ios-voice) 是基于灵云SDK封装了一层。处理音频的转化。

- [CustomBadge](https://github.com/ckteebe/CustomBadge) 是给UIView画角标用。

- [DACircularProgressView](https://github.com/danielamitay/DACircularProgress) 自定义倒计时View。

- [Objective-C-HMTL-Parser](https://github.com/zootreeves/Objective-C-HMTL-Parser) 是一个用 ObjectiveC 编写的简易 HTML 解析器。  

- [QR-Code-Encoder-for-Objective-C](https://github.com/myang-git/QR-Code-Encoder-for-Objective-C) 二维码的生成和扫描。

- [UI7Kit](https://github.com/youknowone/UI7Kit) 是一个iOS7风格GUI工具包补丁。
