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
#### 1、Beacons界面
- 搜索附近的beacon，包括信息有Major，minor， 距离。  
 ![](http://www.markss.cn/images/AprilBeacon/beacons.png) 
 
- 点击进入可以看到beacon距离和rssi强度。
 ![](http://www.markss.cn/images/AprilBeacon/beacon-range.png)

#### 2、工具界面
- 查看周围蓝牙设备（里面包括单个修改beacon参数），批量修改beacon参数，校准beacon距离。
 ![](http://www.markss.cn/images/AprilBeacon/tools.png)  
 
##### 主要说一下工具里面的一些常用功能。  
 其中设备进入可以查看周围有哪些蓝牙设备，在AprilBeacon里面目前暂时只显示名字叫AprilBeacon和BlueBeacon的蓝牙。  
 ![](http://www.markss.cn/images/AprilBeacon/tools-devices.png)  
 点击单个设备进入可以看到设备一些详细信息  
 ![](http://www.markss.cn/images/AprilBeacon/devices-detail.png)  
 点击![](http://www.markss.cn/images/AprilBeacon/device-modified-button.png)可以进入到修改设备参数界面  
 ![](http://www.markss.cn/images/AprilBeacon/tools-device-modifiy.png)  
- ProximimityUUID 格式必须是: ※※※※※※※※-※※※※-※※※※-※※※※-※※※※※※※※※※※※（'※' 字母或者数字， 8位-4位-4位-4位-12位 例如:E2C56DB5-DFFB-48D2-B060-D0F5A71096E0）
- Major 范围是：0-65535
- Minor 范围是：0-65535
- Measured Power 范围是：-255-1
- Tx Power（发射功率）： 0dBm，4dBm，-6dBm，-23dBm四个值。
- 广播频率的范围是：100ms-1000ms
- 新密码：12位  
保存时候需要你输入beacon验证密码（默认为 AprilBrother,注意大小写），修改完成之后会自动重启beacon，无需手动去beacon上按钮重启。

- 批量修改界面如下  
 ![](http://www.markss.cn/images/AprilBeacon/tools-configure.png)  
 ProximimityUUID, major, minor, mesasured Power, 密码格式同上， 其中major， minor可以选择是否自增。 当ProximimityUUID填写后，会自动把周围能搜索到的此uuid的设备信息修改（其中有个注意的地方，如果某个beacon的密码和你修改时候输入的校对密码不一致会导致此个beacon修改失败）。
 密码说明如图:  
 ![](http://www.markss.cn/images/AprilBeacon/confirm-password.png)
 ![](http://www.markss.cn/images/AprilBeacon/new-password.png)
    
#### 3、设置：设置beacon的发射器，后台推送等等。
 ![](http://www.markss.cn/images/AprilBeacon/setting.png)
  