
## 目的
---
- 使用Robit主板控制的mBot迷你小车上的巡迹模块实现沿线跑圈。

## 使用材料
---

- 1 x [Robit智能小车主板](https://www.elecfreaks.com/estore/elecfreaks-robit-diy-mini-smart-cars-robot-development-platform-chassis-for-micro-bit-compatible-with-mbot.html)
- 1 x Mbot Car


## 硬件连接图
---
如上节所示将左右轮电机介入M1，M2端口。
如图所示，将巡迹与Robit主板J2口使用RJ25接线连接。

![](https://i.imgur.com/pQI1cnx.png)

![](https://i.imgur.com/buHExmA.jpg)

![](https://i.imgur.com/LCkSCvZ.jpg)

## 软件
---
[微软makecode](https://makecode.microbit.org/#)

## 编程
---
### 步骤 1
在MakeCode的代码抽屉中点击Advanced，查看更多代码选项。

![](https://i.imgur.com/LjMR5IU.png)

为了给巡迹模块编程，我们需要添加一个代码库。在代码抽屉底部找到“Add Package”，并点击它。这时会弹出一个对话框。搜索“Robit"，然后点击下载这个代码库。

![](https://i.imgur.com/ISZ6w26.png)

注意：如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。

### 步骤 2
在开机启动时初始化巡迹模块端口为J2(P15,P16)，设置左右轮电机到M1，M2端口速度为15。

![](https://i.imgur.com/9yNapu4.png)

设置左右两个红外线传感器的返回值变量Left和right，读取左右红外线传感器的返回参数。

![](https://i.imgur.com/8Ez3dTm.png)

如果右侧红外线传感器检测到脱离黑线，设置左轮速度为5右轮速度为25，向左转。之后设置一个循环，检测小车是否回归到黑线，如果没有就继续向左转直到回到黑线。

![](https://i.imgur.com/BPMSHwa.png)

如果左侧红外线传感器检测到脱离黑线，同理向右转回归黑线。

![](https://i.imgur.com/4F0soRe.png)

### 程序
请参考程序连接：[https://makecode.microbit.org/_9WECsHJmpDxM](https://makecode.microbit.org/_9WECsHJmpDxM)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_9WECsHJmpDxM" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---
**注意：** 可吸收红外光物体均视为黑线。

## 结论
---
mBot小车会沿着预定画好的黑线前进。

![](https://i.imgur.com/15YjRy5.gif)
## 思考
---

## 常见问题
---


## 相关阅读  
---

