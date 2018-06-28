
## 目的
---

- 使用Robit主板控制mBot迷你小车实现倒车报警功能。

## 使用材料
---

- 1 x [Robit智能小车主板](https://www.elecfreaks.com/estore/elecfreaks-robit-diy-mini-smart-cars-robot-development-platform-chassis-for-micro-bit-compatible-with-mbot.html)
- 1 x Mbot Car

## 背景知识
---
### 蜂鸣器

- 蜂鸣器是一种发声器件，它由振动装置和谐振装置组成。按照控制方式分类，可把蜂鸣器又分为有源型与无源型。

- 有源型蜂鸣器的工作发声原理是：蜂鸣器内部集成振荡系统与放大取样电路，当有直流电源通过蜂鸣器时会使谐振装置产生声音信号，有源型蜂鸣器的工作发声原理图如下：

![](https://i.imgur.com/sRjxQfi.jpg)

- 无源型蜂鸣器的工作发声原理是：方波信号输入谐振装置转换为声音信号输出，无源型蜂鸣器的工作发声原理图如下：

![](https://i.imgur.com/Fd2YwUH.jpg)

**注意：**本次实验，我们使用的是无源蜂鸣器。

### 教程目的
- 在[超声波避障](/Robit_Case_02/)中我们实现了使用超声波模块实时检测障碍物，在本节教程中，我们使用超声波模块和蜂鸣器模块实现mBot迷你小车带有声音提醒的倒车雷达功能。

## 硬件连接
---
将左轮电机接入M1端口，右轮电机接入M2端口，超声波模块如前几节教程一样接入J1端口。

![](https://i.imgur.com/foGr3ds.png)

![](https://i.imgur.com/aAEIPxi.jpg)

蜂鸣器所处位置如图所示，接入Micro:Bit的P0端口。

![](https://i.imgur.com/nYUOS8t.png)
## 软件
---
[微软makecode](https://makecode.microbit.org/#)

## 编程
---
### 步骤 1
在MakeCode的代码抽屉中点击Advanced，查看更多代码选项。

![](https://i.imgur.com/LjMR5IU.png)

为了给超声波模块编程，我们需要添加一个代码库。在代码抽屉底部找到“Add Package”，并点击它。这时会弹出一个对话框。搜索“Robit"，然后点击下载这个代码库。

![](https://i.imgur.com/ISZ6w26.png)

注意：如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。

### 步骤 2
开机初始化设置距离变量为away，设置蜂鸣器频率为400Hz，设置左右轮电机分别为M1，M2端口速度为-30。

![](https://i.imgur.com/5LdCdUM.png)

### 步骤3

创建一个forever循环，接收超声波模块返回的数据存入away变量。

如果小车距离墙面是否小于10cm，蜂鸣器长鸣，同时两侧电机都停止。

![](https://i.imgur.com/HfwwKSH.png)


如果小车距离墙面大于10cm且小于50cm，蜂鸣器以1/2节拍蜂鸣，同时设置电机转速为-15。

![](https://i.imgur.com/TaSRDb9.png)

如果小车距离墙面大于50cm，蜂鸣器以4节拍蜂鸣，同时设置电机转速为-30。

![](https://i.imgur.com/ASwsTIA.png)

### 参考程序
参考程序连接：[https://makecode.microbit.org/_gFiciE4PLF37](https://makecode.microbit.org/_gFiciE4PLF37)

你也可以通过下方网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_gFiciE4PLF37" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---
**注意：** 设置速度过低时会造成电机运转不正常。

### 现象
mBot小车在检测到墙面距离大于50cm，蜂鸣器以4节拍蜂鸣，电机全速。

小于50cm大于10cm时，蜂鸣器以1/2节拍蜂鸣，电机速度降低一半慢速前进。

小于10cm，蜂鸣器长鸣，电机停止。

## 思考
---
为什么在停车中要判断距离是否为0？

## 常见问题
---
1. LED点阵显示会严重拖慢程序运行速度，导致小车检测障碍物不及时。

## 相关阅读  
---

