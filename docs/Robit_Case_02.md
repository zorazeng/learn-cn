
## 目的
---

使用Robit主板控制mBot迷你小车实现避障功能。

## 使用材料
---

- 1 x [Robit智能小车主板](https://www.elecfreaks.com/estore/elecfreaks-robit-diy-mini-smart-cars-robot-development-platform-chassis-for-micro-bit-compatible-with-mbot.html)
- 1 x Mbot Car

## 知识提要
---
在[上一节：超声波测距](/Robit_Case_01/)中我们实现了使用超声波模块实时检测距离，在本节教程中，我们使用超声波模块实现mBot迷你小车的避障功能。

## 硬件连接
---
将左轮电机接入M1端口，右轮电机接入M2端口，超声波模块如上节教程一样接入J1端口。

![](https://i.imgur.com/foGr3ds.png)

![](https://i.imgur.com/dVr2oEr.jpg)

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
程序初始化时，定义了一个away变量，用来表示检测到障碍物的距离，并将它置为0。

设置左轮电机M1、右轮电机M2速度均为20。

![](https://i.imgur.com/cNxMb1t.png)

### 步骤3

创建一个forever循环，实时的从J1口读取超声波模块返回的数据，并且赋值给away。

![](https://i.imgur.com/iNreh61.png)

#### 防撞停车
当检测距离(away)距离小于8cm时，停车，暂停300ms后，设置M1，M2为负数实现倒车，延时600ms。


![](https://i.imgur.com/Axkwbms.png)
#### 转向避障
当检测距离(away)距离小于15cm时，生成一个0到100的随机数。

当随机数小于50的时候M1电机赋负值，左轮倒转完成左转。

当随机数大于50的时候M2电机赋负值，右轮倒转完成左转。

![](https://i.imgur.com/DsDXQmg.png)

如果检测距离(away)大于10cm而且不等于0，设置M1和M2速度20前进。

![](https://i.imgur.com/7x5XG1k.png)

### 参考程序
参考程序连接：[https://makecode.microbit.org/_X2g8PfeebXqv](https://makecode.microbit.org/_X2g8PfeebXqv)

你也可以通过下方网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_X2g8PfeebXqv" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  

**注意：** 设置速度过低时会造成电机运转不正常。

### 现象
mBot小车在检测到障碍物距离还有20cm时自动转向，转向后如距离障碍物太近自动倒车。

## 思考
---
为什么在防撞停车中要判断距离是否为0？

## 常见问题
---
**问：为什么开启5X5点阵屏后，会导致无法避障？**

答：LED点阵显示会严重拖慢程序运行速度，导致小车检测障碍物不及时。

## 相关阅读  
---

[Robit简介](Robit_CN)

[Robit教程01_超声波测距](/Robit_Case_01/)

[Robit教程02_超声波避障](/Robit_Case_02/)
