![12](https://i.imgur.com/5RJ1KJn.jpg)   

## 介绍  
---

micro:bit上集成了丰富的传感器，其中就包含了加速度计。在这次的实验中，我们将利用micro:bit上的加速度计来做一个水平仪，并把倾角信号以柱状图形式显示在NeoPixel灯环上。  


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

**加速度计**

在你的micro:bit主板上有一个加速度计。它可以检测micro:bit的速度变化，将模拟信息转换成可以在micro:bit程序中使用的数字格式。输出的单位是毫克。这个装置也可以检测一小部分标准动作，例如：摇晃、倾斜以及自由落体。
 
![](https://i.imgur.com/kzqAOK4.jpg)

加速度计对应的X、Y、Z三个方向如下图所示：

![](https://i.imgur.com/FQ6zBkH.jpg) 


## 硬件连接   
---

按照下图， 完成硬件的连接。
![](https://i.imgur.com/NPvcrUo.jpg)

连接完成后，实物图如下： 
![](https://i.imgur.com/SOD2TLb.jpg) 


## 编程  
---

打开[MakeCode在线编辑器](https://makecode.microbit.org/)，在代码编辑区域中编写代码。建议你先自己尝试着编程。
当然，你可以通过下面这个链接下载程序的完整代码。

[https://makecode.microbit.org/_R2yHPUecyh2i](https://makecode.microbit.org/_R2yHPUecyh2i) 

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_E9UV80hjJKbF" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>


## 代码解释  
---

**show bar graph**
用柱状图的形式显示数值，用法类似于**plot bar graph**。

**Acceleration**
获取三个方向的加速度数值（毫克力），或者所有方向（x、y和z)的合力。


## 实验结果  
---

随着micro:bit的倾斜，灯珠逐个亮起。倾斜角度越大，LED灯珠被点亮的数量越多。

![](https://i.imgur.com/IdpGKQJ.gif)


## 思考   
---

在这个案例中，我们仅仅判断了一个方向（X方向）角度的倾斜，如果我们想测试一个平面的倾斜角度（XY平面），该如何设计电路与编程？欢迎来与我们讨论。

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
[ELECFREAKS Micro:bit Starter Kit Experiment 13:Compass](https://www.elecfreaks.com/10567.html)  
[ELECFREAKS Micro:bit Starter Kit Experiment 14:Ambient light](https://www.elecfreaks.com/10649.html)  
