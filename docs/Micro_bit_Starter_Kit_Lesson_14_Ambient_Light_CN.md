![14](https://i.imgur.com/NkZTTdv.jpg)  
## 介绍  
---

在光敏传感器这个实验里，我们外接一个光敏传感器来感知外界光线，实际上，在micro:bit内部，也集成了一个光敏感应装置，本次实验，我们就用内部集成的光敏感应装置。当外界环境光比较暗时，点亮灯环。  


## 元件清单  
---

### 硬件:

- 1 x [micro:bit](http://www.elecfreaks.com/estore/bbc-micro-bit-board-for-coding-programming.html)
- 1 x USB线
- 1 x [micro:bit面包板扩展板](http://www.elecfreaks.com/estore/microbit-breadboard-adapter.html)
- 1 x [面包板83 x 55 mm](http://www.elecfreaks.com/estore/transparent-breadboard-83-55-mm.html)
- 1 x LED七彩灯环（8颗灯珠）
- 1 x [跳线](http://www.elecfreaks.com/estore/breadborad-jumper-wire-65pcs-pack.html)

**温馨提示：如果你需要以上所有元件，你可以购买我们的[Elecfreaks小小科学家套件](https://item.taobao.com/item.htm?spm=a1z10.1-c-s.w4024-17803785896.2.18dc3f94XOgpWg&id=562837851877&scene=taobao_shop)。**

![](https://i.imgur.com/W4tseua.jpg)

### 软件：

[微软MakeCode在线编辑器](https://makecode.microbit.org/)


## 主要元件介绍  
---

你可能好奇为什么micro:bit没有任何光传感器却能够感光。让我们一起来看看micro:bit官网上关于micro:bit屏幕的一段话：

micro:bit屏幕是由一个5x5的LED点阵构成。它作为一个3x9的矩阵连接到了micro:bit上。运行软件高速反复更新这个矩阵，正因为如此，它是位于用户视野范围内，并且不会检测到任何闪光。通过将一些LED驱动引脚反复切换成输入，并对电压衰减时间进行采样，这个LED矩阵也被应用于感应环境光，这和周围的环境光等级大致成正比。

![](https://i.imgur.com/1JzFZG3.jpg) 

真是太不可思议啦！除了它的发光能力，micro:bit居然可以感光！因为LED通常被作为发光器来使用，所以我们很容易忘记它是基本的光电二极管，而且也是光检测器。如果并入LED驱动电路中，那么它的功能就能够被很好地展现，而无须任何额外的硬件。


## 硬件连接
---

按照下图，完成硬件的连接。
![](https://i.imgur.com/fKgQRoW.jpg)

连接完成后，实物图如下：
![](https://i.imgur.com/Hacl6BL.jpg)


## 编程  
---

打开[MakeCode在线编辑器](https://makecode.microbit.org/)，在代码编辑区域中编写代码。建议你先自己尝试着编程。
当然，你也可以通过下面这个链接下载程序的完整代码。点击右上角的“编辑”，然后再点击右下角的“下载”，你就可以将代码直接下载到micro:bit上了。

[https://makecode.microbit.org/_Ws5gzMYvvM2x](https://makecode.microbit.org/_Ws5gzMYvvM2x)


## 代码解释  
---

**Light Level **
找出你周围环境光的亮度等级（有多亮或多暗）。光线等级0代表黑暗，而255代表明亮。micro:bit用LED屏幕上的一些LED来检测环境光。

**Clear**
将所有七彩灯环上的LED灯珠色值设置为0。

注意：把LED当做光敏传感器这种方式实际上并不太灵敏，通常需要比较亮的光线light level的数值才会发生变化。


## 实验结果  
---

在暗处，灯环点亮；在亮处，灯环熄灭。

![](https://i.imgur.com/F9B9ySD.gif)


## 思考   
---

当灯环亮起彩虹色后，让彩虹转动起来。该如何设计电路与编程？欢迎来与我们讨论。

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
[ELECFREAKS Micro:bit Starter Kit Experiment 10:Motor](https://www.elecfreaks.com/10362.html)  
[ELECFREAKS Micro:bit Starter Kit Experiment 11:Rainbow](https://www.elecfreaks.com/10508.html)  
[ELECFREAKS Micro:bit Starter Kit Experiment 12:Accelerometer](https://www.elecfreaks.com/10529.html)  
[ELECFREAKS Micro:bit Starter Kit Experiment 13:Compass](https://www.elecfreaks.com/10567.html)  
[ELECFREAKS Micro:bit Starter Kit Experiment 14:Ambient light](https://www.elecfreaks.com/10649.html)

   

