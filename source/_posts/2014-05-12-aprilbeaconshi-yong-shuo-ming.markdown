---
layout: post
title: "AprilBeacon使用说明"
date: 2014-05-12 09:50:58 +0800
comments: true
categories: 
---

# [AprilBeacon](https://itunes.apple.com/cn/app/aprilbeacon/id847517010?mt=8)介绍
## 软件主要分为三大模块。 
### 1、Beacons界面
- 搜索附近的beacon，包括信息有Major，minor，距离，Rssi。  
![](http://www.markss.cn/images/AprilBeacon/beacons.png) 
 
- 点击进入可以看到beacon距离和rssi强度。  
![](http://www.markss.cn/images/AprilBeacon/beacon-range.png)

### 2、工具界面
- 查看周围蓝牙设备（里面包括单个修改beacon参数），批量修改beacon参数，校准beacon距离。
![](http://www.markss.cn/images/AprilBeacon/tools.png)  
 
#### 2.1 周围蓝牙设备
- 可以查看周围有哪些蓝牙设备，在AprilBeacon里面只列出名字叫AprilBeacon和BlueBeacon的设备。  
![](http://www.markss.cn/images/AprilBeacon/tools-devices.png)  
 
- 点击单个设备进入可以看到设备详细信息。  
![](http://www.markss.cn/images/AprilBeacon/devices-detail.png)  
 
- 点击![](http://www.markss.cn/images/AprilBeacon/device-modified-button.png)可以进入到修改单个设备参数界面  
![](http://www.markss.cn/images/AprilBeacon/tools-device-modifiy.png)  
- ProximimityUUID 格式必须是: ########-####-####-################（'#' 字母或者数字 8位-4位-4位-4位-12位 例如:E2C56DB5-DFFB-48D2-B060-D0F5A71096E0）。
- Major 范围是：0-65535。
- Minor 范围是：0-65535。
- Measured Power 范围是：-255-1。
- Tx Power（发射功率）： 0dBm，4dBm，-6dBm，-23dBm四个值。
- 广播频率的范围是：100ms-1000ms。
- 新密码：12位。  
保存时候需要你输入beacon验证密码（默认为 AprilBrother,注意大小写），修改完成之后会自动重启beacon，无需手动去beacon上按钮重启。

#### 2.2 批量修改界面
- 可以批量更改设备ProximityUUID，Major，Minor，Measured Power，密码。ProximimityUUID, major, minor, mesasured Power, 密码格式同上面单个修改一致，增加了major， minor可以选择是否自增。 当ProximimityUUID填写后，会自动把周围能搜索到的此uuid的设备信息修改。（其中有个注意的地方，如果某个beacon的密码和你修改时候输入的校对密码不一致会导致此个beacon修改失败)  
![](http://www.markss.cn/images/AprilBeacon/tools-configure.png)  
 
- 密码说明如图  
![](http://www.markss.cn/images/AprilBeacon/new-password.png)  
![](http://www.markss.cn/images/AprilBeacon/confirm-password.png)  

#### 2.3 校准界面
- 校准界面能搜索到附近的beacons按 未知，远， 近, 排列，点击beacon可以进入校准操作，校准完成之后会得到合适measured power值。
![](http://www.markss.cn/images/AprilBeacon/calibration1.png)  
![](http://www.markss.cn/images/AprilBeacon/calibration2.png)  
    
### 3、设置界面
- 设置界面主要有开启后台推送功能，手机靠近或者离开beacon区域时候开启，是否显示事例通知。  
![](http://www.markss.cn/images/AprilBeacon/setting.png)  

- 配置beacon筛选器，发射器。只有配置了过的ProximityUUID才可以在Beacons界面被搜索出来。  
![](http://www.markss.cn/images/AprilBeacon/transmitters.png)  
![](http://www.markss.cn/images/AprilBeacon/new-transmitters.png)
  