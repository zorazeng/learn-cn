
## 目的
---

- 了解什么是超声波，如何用超声波测距。
- 使用Robit主板控制的mBot迷你小车上的超声波模块来测距。

## 使用材料
---

- 1 x [Robit智能小车主板](https://www.elecfreaks.com/estore/elecfreaks-robit-diy-mini-smart-cars-robot-development-platform-chassis-for-micro-bit-compatible-with-mbot.html)
- 1 x Mbot Car

## 背景知识
---
### 什么是超声波
[超声波](https://zh.wikipedia.org/wiki/%E8%B6%85%E8%81%B2%E6%B3%A2)是一种频率高于20000赫兹的声波，它的方向性好，穿透能力强，易于获得较集中的声能，在水中传播距离远，可用于测距、测速、清洗、焊接、碎石、杀菌消毒等。超声波因其频率下限大于人的听觉上限而得名。

### 超声波测距原理
超声波发射器向某一方向发射超声波，在发射时刻的同时开始计时，超声波在空气中传播，途中碰到障碍物就立即返回来，超声波接收器收到反射波就立即停止计时。根据接收器接到超声波时的时间计算距离，与雷达测距原理相似。

![](https://i.imgur.com/vSFTiuw.jpg)



## 硬件连接图
---

如图所示，将超声波模块与Robit主板J1口使用RJ25接线链接

![](https://i.imgur.com/pQI1cnx.png)
![](https://i.imgur.com/zFWVN9O.jpg)

## 软件
---
[微软makecode](https://makecode.microbit.org/#)

## 编程
---
### 步骤 1
在MakeCode的代码抽屉中点击Advanced，查看更多代码选项。

![](https://i.imgur.com/LjMR5IU.png)

为了给超声波模块编程，我们需要添加一个代码库。在代码抽屉底部找到“Add Package”，并点击它。这时会弹出一个对话框。搜索`Robit`，然后点击下载这个代码库。

![](https://i.imgur.com/ISZ6w26.png)

注意：如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。

### 步骤 2

在`Basic`中拖出一个`forever`积木块，在其中插入`show number`积木块。

在Robit中拖出Ultrasonic pin积木块，选择J1(P13,P14)。这条语句作用为读取超声波模块返回参数。
![](https://i.imgur.com/hwrw0c8.png)


### 程序
请参考程序连接：[https://makecode.microbit.org/_3ktFD2gabF7J](https://makecode.microbit.org/_3ktFD2gabF7J)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_3ktFD2gabF7J" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  

**注意：** 该超声波模块检测的最大距离大约为400cm。

### 现象
超声波模块会实时返回距离，并且显示在Micro:bit的5X5点阵上，距离单位为厘米CM。

![](https://i.imgur.com/jAFZNHU.jpg)

## 思考
---
超声波测距显示距离为0有几种情况？

## 常见问题
---


## 相关阅读  
---

