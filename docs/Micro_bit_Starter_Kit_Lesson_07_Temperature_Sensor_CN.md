![7](https://i.imgur.com/fMCJitN.jpg)

## 介绍
---

温度传感器是指能感受温度并转换成可用输出信号的传感器。温度传感器是温度测量仪表的核心部分，品种繁多。在这次的实验中，我们将学习模拟温度传感器——TMP36，并将它的数值读出显示在micro:bit的显示屏上。


## 元件清单  
---

### 硬件：

1 x [micro:bit](http://www.elecfreaks.com/estore/bbc-micro-bit-board-for-coding-programming.html)
1 x USB线
1 x [microbit面包板扩展板](http://www.elecfreaks.com/estore/microbit-breadboard-adapter.html)
1 x [面包板83 x 55 mm](http://www.elecfreaks.com/estore/transparent-breadboard-83-55-mm.html)
1 x TMP36温度传感器
1 x [跳线](http://www.elecfreaks.com/estore/breadborad-jumper-wire-65pcs-pack.html)

**温馨提示：如果你需要以上所有元件，你可以购买我们的[Elecfreaks小小科学家套件](https://item.taobao.com/item.htm?spm=a1z10.1-c-s.w4024-17803785896.2.18dc3f94XOgpWg&id=562837851877&scene=taobao_shop)。**

![](https://i.imgur.com/W4tseua.jpg)

### 软件：

[微软MakeCode在线编辑器](https://makecode.microbit.org/)


## 主要元件介绍  
---

### TMP36

TMP36是一种模拟温度传感器，它的输出电压与温度成线性关系，温度越高，输出电压越大。

![](https://i.imgur.com/SDoXRcM.jpg)

**注意：**

当我们正视TMP36芯片有文字的一面时，芯片最左边的引脚为VCC，中间引脚为Vout，最右边的引脚为GND。千万不要把芯片接反了，否则也能引起器件损坏。

![](https://i.imgur.com/P6ZkUDh.jpg)

TMP36输出电压随温度变化的曲线是这样的：

![](https://i.imgur.com/5R7izFc.jpg)
![](https://i.imgur.com/U2c4qdp.jpg)

由上图可知温度的计算公式为：

温度（℃）=（输出电压(mV) - 500 ) / 10


## 硬件连接  
---

按照下图, 完成硬件的连接。
![](https://i.imgur.com/HnUeLBR.jpg)

连线完成后，实物图如下：
![](https://i.imgur.com/IAor80B.jpg)


## 编程
---

打开[MakeCode在线编辑器](https://makecode.microbit.org/)，在代码编辑区域中编写代码。建议你先自己尝试着编程。
当然，你也可以通过下面这个页面查看程序的完整代码。点击右上角的“编辑”，然后再点击右下角的“下载”，你就可以将代码直接下载到micro:bit上了。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_7MLCRdhek0mJ" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>


## 代码解释  
---

**map**

Map是把一个具体的数值从一个范围映射到另一个范围。这个函数把from low的数值映射到to low的值中， 把from high的数值映射到to high的值中，并且把中间的数值映射到中间的数值中。
这个函数不限制数值范围，因为有时超出范围的数值是必要的和有用的。 如果你需要限制数值在一个范围内，你可以在引用此函数之前或之后使用Math.clamp函数。

![](https://i.imgur.com/oCPoKPs.jpg)

在程序中，先利用map积木块将读取的模拟数值转化为电压（mV）值。
**analog read**读取的数值为0至1023，故**from low**为0，**from high**为1023。
micro:bit的基准电压为3.3V，即3300Mv。故**to low**为0，**to high**为3300。

![](https://i.imgur.com/b8aM1qv.jpg)

温度（℃）=（输出电压(mV) - 500 ) / 10

根据上述公式计算出温度值。 


## 实验结果  
---

micro:bit屏幕上显示当前温度值。
![](https://i.imgur.com/b0w5PkN.gif)


## 思考  
---

这次实验micro:bit显示的为摄氏温度，如果想要显示华氏温度，我们该如何设计电路与编程呢？欢迎来与我们讨论。

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
[ELECFREAKS Micro:bit Starter Kit Experiment 08:Servo](https://www.elecfreaks.com/10221.html)
[ELECFREAKS Micro:bit Starter Kit Experiment 09:Buzzer](https://www.elecfreaks.com/10318.html)
[ELECFREAKS Micro:bit Starter Kit Experiment 10:Motor](https://www.elecfreaks.com/10362.html)
[ELECFREAKS Micro:bit Starter Kit Experiment 11:Rainbow](https://www.elecfreaks.com/10508.html)
[ELECFREAKS Micro:bit Starter Kit Experiment 12:Accelerometer](https://www.elecfreaks.com/10529.html)
[ELECFREAKS Micro:bit Starter Kit Experiment 13:Compass](https://www.elecfreaks.com/10567.html)
[ELECFREAKS Micro:bit Starter Kit Experiment 14:ambient light](https://www.elecfreaks.com/10649.html)

