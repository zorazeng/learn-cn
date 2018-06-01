![11](https://i.imgur.com/F2gbRrO.jpg)    

## 介绍  
---

LED七彩灯环是基于ws2812b灯珠。它的最大特点是单IO控制与无限级联。在这次的实验中，我们将用micro:bit来驱动灯环实现彩虹色渐变。


## 元件清单  
---

### 硬件:  

- 1 x [micro:bit](http://www.elecfreaks.com/estore/bbc-micro-bit-board-for-coding-programming.html)
- 1 x USB线
- 1 x [micro:bit面包板扩展板](http://www.elecfreaks.com/estore/microbit-breadboard-adapter.html)
- 1 x [面包板 83 x 55 mm](http://www.elecfreaks.com/estore/transparent-breadboard-83-55-mm.html)
- 1 x LED七彩灯环（8颗灯珠）
- 1 x [跳线](http://www.elecfreaks.com/estore/breadborad-jumper-wire-65pcs-pack.html)

**温馨提示：如果你需要以上所有元件，你可以购买我们的[Elecfreaks小小科学家套件](https://item.taobao.com/item.htm?spm=a1z10.1-c-s.w4024-17803785896.2.18dc3f94XOgpWg&id=562837851877&scene=taobao_shop)。**

![](https://i.imgur.com/W4tseua.jpg)

### 软件：

[微软MakeCode在线编辑器](https://makecode.microbit.org/)


## 主要元件介绍
---

**LED七彩灯环（8颗灯珠）**

![](https://i.imgur.com/NnNcXY9.jpg)

LED七彩灯环（8颗灯珠）是由8颗ws2812b灯珠级联而成的灯环，ws2812b是一个集控制电路与发光电路于一体的智能外控LED光源，其外型与一个5050LED灯珠相同。

像素点内部包含了智能数字接口数据锁存信号整形放大驱动电路，还包含有高精度的内部振荡器和12V高压可编程定电流控制部分，有效保证了像素点光的颜色高度一致。

数据协议采用单线归零码的通讯方式，像素点在上电复位以后，DIN端接受从控制器传输过来的数据，首先送过来的24bit数据被第一个像素点提取后，送到像素点内部的数据锁存器，剩余的数据经过内部整形处理电路整形放大后通过DO端口开始转发输出给下一个级联的像素点，每经过一个像素点的传输，信号减少24bit。像素点采用自动整形转发技术，使得该像素点的级联个数不受信号传送的限制，仅仅受限信号传输速度要求。

LED具有低电压驱动，环保节能，亮度高，散射角度大，一致性好，超低功率，超长寿命等优点。将控制电路集成于LED上面，电路变得更加简单，体积小，安装更加简便。


## 硬件连接  
---

按照下图， 完成硬件的连接。
![](https://i.imgur.com/LAPXCJp.jpg)

注意：灯环引出了两组线，一组是DI,另一组是DO，我们应当连接DI这一组。

连接完成后，实物图如下： 
![](https://i.imgur.com/lUdmz6q.jpg)  


## 编程  
---

打开[MakeCode在线编辑器](https://makecode.microbit.org/)，在代码编辑区域中编写代码。建议你先自己尝试着编程。
在这次的实验中，我们将会添加一个代码库来方便我们使用LED七彩灯环。在代码抽屉中点击Advanced（高级）来查看更多代码选项，并在底部找到Add Package(添加代码库）。

![](https://i.imgur.com/FwzImaX.gif)

当然，你也可以通过下面这个链接下载程序的完整代码。点击右上角的“编辑”，然后再点击右下角的“下载”，你就可以将代码直接下载到micro:bit上了。
[https://makecode.microbit.org/_cvrLAKeJC2yT](https://makecode.microbit.org/_cvrLAKeJC2yT)


## 代码解释  
---

**set to NeoPixel **

**set to NeoPixel**用于初始化灯，其中有三个参数需要设置：**pin**设置连接灯带的引脚；**with x leds**设置灯珠的数量；**as RGB**设置灯珠的类型。

**show rainbow**

用于把灯带设置成彩虹渐变。

**show**

设置好了LED的颜色后，不代表它就会开始工作。为了让它真正工作，你需要使用**show**。

**sotate pixels**

按环形移位灯珠的颜色信息。


## 实验结果  
---

我们可以看到LED彩虹灯环实现了运动的彩虹渐变效果。

![](https://i.imgur.com/23vhDKK.gif)


## 思考   
---

想象灯环是一只大眼睛，让灯环显示眨眼睛的效果，那么我们该如何设计电路与编程？欢迎来与我们讨论。

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
[ELECFREAKS Micro:bit Starter Kit Experiment 12:Accelerometer](https://www.elecfreaks.com/10529.html)
[ELECFREAKS Micro:bit Starter Kit Experiment 13:Compass](https://www.elecfreaks.com/10567.html)
[ELECFREAKS Micro:bit Starter Kit Experiment 14:ambient light](https://www.elecfreaks.com/10649.html)