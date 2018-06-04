![10](https://i.imgur.com/8KZyoCy.jpg)

## 介绍  
---

电机是依据电磁感应定律实现电能转换为动能的一种装置。在这次的实验中，我们将用一个开关来控制电机的启动与停止。


## 元件清单  
---

### 硬件:  

- 1 x [micro:bit](http://www.elecfreaks.com/estore/bbc-micro-bit-board-for-coding-programming.html)
- 1 x USB线
- 1 x [micro:bit面包板扩展板](http://www.elecfreaks.com/estore/microbit-breadboard-adapter.html)
- 1 x [面包板83 x 55 mm](http://www.elecfreaks.com/estore/transparent-breadboard-83-55-mm.html)
- 1 x 5V 迷你电机
- 1 x TIP 120 NPN 三极管
- 1 x 1N4007 二极管
- 1 x 100 欧姆电阻
- 1 x [跳线](http://www.elecfreaks.com/estore/breadborad-jumper-wire-65pcs-pack.html)
- 2 x 鳄鱼夹线

**温馨提示：如果你需要以上所有元件，你可以购买我们的[Elecfreaks小小科学家套件](https://item.taobao.com/item.htm?spm=a1z10.1-c-s.w4024-17803785896.2.18dc3f94XOgpWg&id=562837851877&scene=taobao_shop)。**

![](https://i.imgur.com/W4tseua.jpg)

### 软件：

[微软MakeCode在线编辑器](https://makecode.microbit.org/)


## 主要元件介绍
---

### 电机

电机是依据电磁感应定律实现电能转换为动能的一种装置。电机的分类非常多，在本案例里，我们用到的是直流电机。当在电机两端加上直流电压时，电机会旋转，电压越高，旋转的速度越快。

![](https://i.imgur.com/JesPIk4.jpg)

### 二极管

二极管是一种具有两个电极的原件，一端为阳极，一端为阴极，它只允许电流从阳极向阴极方向移动，可以把它想象成电子版的止逆阀。
对于普通的二极管，可以通过管体表面颜色来区分正负极，有白线的一端为负极。

![](https://i.imgur.com/b1g3bBJ.jpg)

### 鳄鱼夹线

鳄鱼夹线与跳线的作用一样。有些器件不方便用跳线连接，可以考虑用鳄鱼夹来连线。

![](https://i.imgur.com/EfkdKmY.jpg)

本次实验，我们就是用鳄鱼夹线来连接我们的电机。

![](https://i.imgur.com/Oj1aUaf.jpg)


## 硬件连接  
---

按照下图， 完成硬件的连接。

![](https://i.imgur.com/2MZA7bj.jpg)

micro:bit的IO口的驱动电流非常微弱的，不足以直接驱动电机。这时候，我们就需要用到三极管将IO信号的电流放大，用三极管放大IO口信号电流的电路图与上一课驱动蜂鸣器的电路图非常类似，唯一的区别是在电机两端加上了一个二极管。该二极管在此电路中叫做续流二极管。

电机里面有线圈，线圈在通过电流时，会在其两端产生感应电动势。当电流消失时，其感应电动势会对电路中的元件产生反向电压，有可能会损坏器件，续流二极管在电路中反向并联在线圈的两端，当电感线圈断电时其两端的电动势并不立即消失，此时残余电动势通过二极管释放。这是一种经典保护设计。

三极管将IO信号的电流放大的局部电路图如下： 

![](https://i.imgur.com/e4YL3hx.jpg)

连接完成后，实物图如下： 

![](https://i.imgur.com/RwH4uNp.jpg) 


## 编程  
---

打开[MakeCode在线编辑器](https://makecode.microbit.org/)，在代码编辑区域中编写代码。建议你先自己尝试着编程。
当然，你也可以通过下面这个链接查看程序的完整代码。点击右上角的“编辑”，然后再点击右下角的“下载”，你就可以将代码直接下载到micro:bit上了。

[https://makecode.microbit.org/_Kid26LToz2mU](https://makecode.microbit.org/_Kid26LToz2mU)

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_MwaF0ALKiP5c" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>


## 代码解释  
---

在软件方面，本实验没有涉及到新的知识点。
本实验特别要注意的是P1口连接的是按钮，在on start积木块里，一定要设置P1口为上拉模式，否则可能无法正确识别按钮信号。

![](https://i.imgur.com/7lkYPlA.jpg)


## 实验结果  
---

按下按钮时，电机开始旋转，再按一次，电机停止旋转。
注意：micro:bit的电源电压比较低，只有3V，按下按钮时，电机有可能不能启动，遇到这种情况，请用手拨动一下电机的扇叶，电机方能正常旋转。

![](https://i.imgur.com/UeWUgLi.gif)


## 思考   
---

如果要用电位器对电机进行速度控制，该如何设计电路与编程？欢迎来与我们讨论。

## 常见问题
---


## 相关阅读  
---

[Start Your Micro:bit Programming Trip](https://www.elecfreaks.com/9299.html)
[ELECFREAKS Micro:bit Starter Kit Experiment 01:LED](https://www.elecfreaks.com/9784.html)
[ELECFREAKS Micro:bit Starter Kit Experiment 02:Button](https://www.elecfreaks.com/9825.html)
[ELECFREAKS Micro:bit Starter Kit Experiment 03:Trimpot](https://www.elecfreaks.com/9879.html)
[ELECFREAKS Micro:bit Starter Kit Experiment 04:Photocell](https://www.elecfreaks.com/9909.html)
[ELECFREAKS Micro:bit Starter Kit Experiment 05:RGB LED](https://www.elecfreaks.com/9978.html)
[ELECFREAKS Micro:bit Starter Kit Experiment 06:Self-lock Switch](https://www.elecfreaks.com/10061.html)
[ELECFREAKS Micro:bit Starter Kit Experiment 07:Temperature Sensor](https://www.elecfreaks.com/10166.html)
[ELECFREAKS Micro:bit Starter Kit Experiment 08:Servo](https://www.elecfreaks.com/10221.html)
[ELECFREAKS Micro:bit Starter Kit Experiment 09:Buzzer](https://www.elecfreaks.com/10318.html)
[ELECFREAKS Micro:bit Starter Kit Experiment 11:Rainbow](https://www.elecfreaks.com/10508.html)
[ELECFREAKS Micro:bit Starter Kit Experiment 12:Accelerometer](https://www.elecfreaks.com/10529.html)
[ELECFREAKS Micro:bit Starter Kit Experiment 13:Compass](https://www.elecfreaks.com/10567.html)
[ELECFREAKS Micro:bit Starter Kit Experiment 14:ambient light](https://www.elecfreaks.com/10649.html)