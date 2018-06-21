
## 目的
---

- 了解巡迹模块，认识巡迹模块。
- 使用Robit主板控制的mBot迷你小车上的巡迹模块实现边缘检测。

## 使用材料
---

- 1 x [Robit智能小车主板](https://www.elecfreaks.com/estore/elecfreaks-robit-diy-mini-smart-cars-robot-development-platform-chassis-for-micro-bit-compatible-with-mbot.html)
- 1 x Mbot Car

## 背景知识
---
### 巡迹模块原理

- 该巡迹模块使用的为[红外线传感器](https://baike.baidu.com/item/%E7%BA%A2%E5%A4%96%E7%BA%BF%E4%BC%A0%E6%84%9F%E5%99%A8/9007351?fr=aladdin),模块由一个**发射端**和一个**接收端**组成，发射端发射红外线由地面反射回来由接收端接收。
- 遇到黑色地面或者其他吸收红外光材质的物品时，接收端无法接收到红外线，巡迹模块返回1。

![](https://i.imgur.com/8UN8B88.jpg)

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

如果左右红外线中至少有一个没收到反馈(检测到边缘)，设置左右电机速度为负数倒车。
随机生成一个0到100的数，如果小于50，停止电机M1完成右转向，如果大于50，停止电机M2完成左转向。

![](https://i.imgur.com/gpsfDps.png)

如果左右红外线传感器均未检测到，设置左右电机速度为15继续前进。

![](https://i.imgur.com/OCspxD3.png)
### 程序
请参考程序连接：[https://makecode.microbit.org/_1mCg9TgVxJ5K](https://makecode.microbit.org/_1mCg9TgVxJ5K)

你也可以通过以下网页直接下载程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_1mCg9TgVxJ5K" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  

**注意：** 可吸收红外光物体均视为黑线。

## 现象
---
mBot小车会检测到桌面边缘后退防止掉落。

![](https://i.imgur.com/u7fGgG1.gif)

## 思考
---

## 常见问题
---


## 相关阅读  
---

