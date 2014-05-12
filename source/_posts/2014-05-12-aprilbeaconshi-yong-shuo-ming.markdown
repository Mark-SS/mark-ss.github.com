---
layout: post
title: "AprilBeacon使用说明"
date: 2014-05-12 09:50:58 +0800
comments: true
categories: 
---

# 软件简介
## 软件介绍
### 软件主要分为三大模块。 
#### 1、Beacons：主要负责搜索附近的beacon。
#### 2、工具：主要可以修改beacon的一些参数。 
#### 3、设置：设置beacon的发射器，后台推送等等。
- 1、Beacons界面。  
 ![](http://www.markss.cn/images/AprilBeacon/beacons.png)  

- 2、工具界面。  
 ![](http://www.markss.cn/images/AprilBeacon/tools.png)  
 ##### 主要说一下工具里面的一些常用功能。  
 其中设备进入可以查看周围有哪些蓝牙设备，在AprilBeacon里面目前暂时只显示名字叫AprilBeacon和BlueBeacon的蓝牙。  
 ![](http://www.markss.cn/images/AprilBeacon/tools-devices.png)  
 点击单个设备进入可以看到设备一些详细信息  
 ![](http://www.markss.cn/images/AprilBeacon/devices-detail.png)  
 点击![](http://www.markss.cn/images/AprilBeacon/device-modified-button.png)可以进入到修改设备参数界面  
 ![](http://www.markss.cn/images/AprilBeacon/tools-device-modifiy.png)  
- ProximimityUUID 格式必须是 ********-****-****-****-************（'*' 字母或者数字， 8位-4位-4位-4位-12位）
- Major 范围是：0-65535
- Minor 范围是：0-65535
- Measured Power 范围是：-255--1
- Tx Power（发射功率）： 0dBm，4dBm，-6dBm，-23dBm四个值。
- 广播频率的范围是：100ms-1000ms
- 新密码：12位  
保存时候需要你输入beacon验证密码（默认为 AprilBrother,注意大谢谢）。
    
- 3、设置界面。  
 ![](http://www.markss.cn/images/AprilBeacon/setting.png)
  