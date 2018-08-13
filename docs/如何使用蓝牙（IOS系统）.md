
## 目的
---

- 在IOS系统下使用蓝牙连接Micro:bit主板。

## 使用材料
---

- 1 x [Micro:bit](https://www.elecfreaks.com/estore/micro-bit-board-with-battery-holder-kit-836.html)
- 1 x IOS系统平台

## 背景知识
---

- [Micro:bit](http://microbit.org/)是一个小型的可编程计算机，由英国广播电视公司（BBC）推出，专为青少年编程教育，设计旨在使学习与教学变得轻松有趣。

- [IOS](https://baike.baidu.com/item/iOS/45705#viewPageContent)是由苹果公司开发的移动操作系统 。苹果公司最早于2007年1月9日的Macworld大会上公布这个系统，最初是设计给iPhone使用的，后来陆续套用到iPod touch、iPad以及Apple TV等产品上。

- [蓝牙（ Bluetooth® ）](https://baike.baidu.com/item/%E8%93%9D%E7%89%99/102670?fr=aladdin)：是一种无线技术标准，可实现固定设备、移动设备和楼宇个人域网之间的短距离数据交换（使用2.4—2.485GHz的ISM波段的UHF无线电波），蓝牙可连接多个设备，克服了数据同步的难题。

- [Bittysoftware](http://www.bittysoftware.com/index.html)：提供与BBC micro：bit等设备配合使用的智能手机应用程序及工具。

- [nRF connect](http://www.nordicsemi.com/chi_simple) NRF连接是一个功能强大的通用工具，它可以让您扫描，宣传和探索你的蓝牙低功耗（BLE）设备和与他们沟通。

## 软件准备
---

![](https://i.imgur.com/aX7znnU.png)

- nRf connect，在APP store中搜索nRF connect，并且下载。软件界面如图所示： 

![](https://i.imgur.com/5c16XJv.png) ![](https://i.imgur.com/nHKuD86.png)

-  Bitty Blue，在APP store中搜索Bitty Blue，并且下载。软件界面如图所示：

![](https://i.imgur.com/VFrFti5.png) ![](https://i.imgur.com/hmym0Xv.png)

## 程序
---
### 步骤 1：添加代码包
在MakeCode的代码抽屉中点击Advanced，查看更多代码选项。

![](https://i.imgur.com/LjMR5IU.png)

为了给蓝牙模块编程，我们需要添加一个代码库。在代码抽屉底部找到“Add Package”，并点击它。这时会弹出一个对话框。搜索“bluetooth"，然后点击下载这个代码库。

![](https://i.imgur.com/ZNxv964.png)

注意：如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。

### 步骤 2：编码

在系统上电开机的时候启动蓝牙按键服务，在蓝牙连接时显示字符"T"，断开蓝牙连接时显示字符"F"。

![](https://i.imgur.com/WmMlkNr.png)

参考程序连接：[https://makecode.microbit.org/_Dyu4j2A4F23c](https://makecode.microbit.org/_Dyu4j2A4F23c)

## 设置蓝牙模式
---

开启micro:bit的蓝牙模式，需要同时按下按键A＋B然后按一下reset键，5X5点阵会显示 **`PAIRING MODE！`** 和一个特殊符号，特殊符号每个microbit都不同，为蓝牙的特殊标识符。
<br></br>
<br></br>
![](https://i.imgur.com/hlt1jqD.jpg) ![](https://i.imgur.com/aqmIAwY.jpg)

## IOS系统配对蓝牙
---

- 打开nRF connect，找到类似BBC micro:bit[xxxxx]蓝牙设备，点击【CONNECT】按钮。会弹出蓝牙配对请求。

![](https://i.imgur.com/QinTNv6.png) ![](https://i.imgur.com/K2Xbila.png)

- 点击配对后完成蓝牙配对，Micro:bit板显示一个√。

![](https://i.imgur.com/pbSFZZ8.jpg)

- 配对成功后Micro:bit会重启。

## 连接蓝牙
---

打开Bitty Blue，点击【Scan】按钮获取已配对蓝牙设备，点击设备完成蓝牙连接，Micro:bit显示字符"T"，APP进入主界面。

![](https://i.imgur.com/i9mucj8.png) ![](https://i.imgur.com/0KauZdY.png)

![](https://i.imgur.com/8YJdwQG.jpg)


点击相应图标，即可测试相应功能。

**注意：**因在程序中仅开启了蓝牙按键功能，故本教程只能使用【Animal Magic】测试按键，其他功能会报错。如需测试其他功能请在程序中开启。

## 断开蓝牙
---

退出APP，或者IOS设备关闭蓝牙开关等操作都会断开蓝牙连接。Micro:bit显示字符"F"。

![](https://i.imgur.com/jcv7YrD.jpg)


## 思考
---

在蓝牙模式下测试Micro:bit其他模块功能该如何编写代码？

## 常见问题
---

**问：为什么修改完程序重新启动无法连接？**

答：每次Micro:bit重新启动都需要重新配对，首先到IOS设备蓝牙中忽略(忘记)此设备，然后重新配对蓝牙。

**问：无法下载nRF connect应用软件**

答：其他类似蓝牙连接软件均可实现，本教程仅供参考。


## 相关阅读  
---

[Bitty blue使用手册](http://www.bittysoftware.com/apps/bitty_blue.html)
