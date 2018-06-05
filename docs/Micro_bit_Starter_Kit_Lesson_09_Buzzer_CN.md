![9](https://i.imgur.com/nCSnCEt.jpg)  

## 介绍  
---

蜂鸣器是一种一体化结构的电子讯响器，广泛应用于计算机、打印机、复印机、报警器、电子玩具、汽车电子设备、电话机、定时器等电子产品中作发声器件。本次实验，我们用micro:bit驱动蜂鸣器，让它发出不同的声音的高频与低频间来回循环，就像警报声一样，并且在micro:bit屏幕上以柱形图的形式显示声音频率。


## 元件清单  
---

### 硬件:

- 1 x [micro:bit](http://www.elecfreaks.com/estore/bbc-micro-bit-board-for-coding-programming.html)
- 1 x USB线
- 1 x [microbit面包板扩展板](http://www.elecfreaks.com/estore/microbit-breadboard-adapter.html)
- 1 x [面包板83 x 55 mm](http://www.elecfreaks.com/estore/transparent-breadboard-83-55-mm.html)
- 1 x 蜂鸣器
- 1 x TIP 120 NPN 三极管
- 1 x 100 欧姆电阻
- 1 x [跳线](http://www.elecfreaks.com/estore/breadborad-jumper-wire-65pcs-pack.html)

**温馨提示：如果你需要以上所有元件，你可以购买我们的[Elecfreaks小小科学家套件](https://item.taobao.com/item.htm?spm=a1z10.1-c-s.w4024-17803785896.2.18dc3f94XOgpWg&id=562837851877&scene=taobao_shop)。**

![](https://i.imgur.com/W4tseua.jpg)

## 软件：

[微软MakeCode在线编辑器](https://makecode.microbit.org/)


## 主要元件介绍
---

### 蜂鸣器  

蜂鸣器是一种发声器件，它由振动装置和谐振装置组成。按照控制方式分类，可把蜂鸣器又分为有源型与无源型。  

![](https://i.imgur.com/KfDVHIk.jpg)
 
有源型蜂鸣器的工作发声原理是：蜂鸣器内部集成振荡系统与放大取样电路，当有直流电源通过蜂鸣器时会使谐振装置产生声音信号，有源型蜂鸣器的工作发声原理图如下：

![](https://i.imgur.com/spNnKiB.jpg) 

无源型蜂鸣器的工作发声原理是：方波信号输入谐振装置转换为声音信号输出，无源型蜂鸣器的工作发声原理图如下：

![](https://i.imgur.com/kNHyjjl.jpg)

注：本次实验，我们使用的是无源蜂鸣器。

### 三极管

三极管是一种控制电流的半导体器件，其作用是把微弱信号放大成幅度值较大的电信号。

![](https://i.imgur.com/LEvAFS5.jpg)

如果直接把micro:bit产生的PWM信号输入至蜂鸣器，蜂鸣器只会发出微弱的声音，这是因为IO口的驱动电流通常都是非常微弱的，不足以直接驱动蜂鸣器这类器件。这时候，我们就需要用到三极管将PWM信号的电流放大，从而让蜂鸣器能发出正常的声响。
用三极管驱动蜂鸣器，典型应用电路如下：

![](https://i.imgur.com/ZhQ3fhv.jpg)


## 硬件连接  
---

按照下图，完成硬件的连接。
![](https://i.imgur.com/YTNuh7H.jpg)

连接完成后，实物图如下：
![](https://i.imgur.com/iYiZM7O.jpg)


## 编程  
---

打开[MakeCode在线编辑器](https://makecode.microbit.org/)，在代码编辑区域中编写代码。建议你先自己尝试着编程。
当然，你也可以通过下面这个页面查看程序的完整代码。点击右上角的“编辑”，然后再点击右下角的“下载”，你就可以将代码直接下载到micro:bit上了。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_02rM94DCp8De" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>


## 代码解释  
---

**Analog Set Period**

配置指定模拟引脚的脉冲宽度调节（PWM）周期。在你调用这个函数之前，你应该将指定的引脚设置为模拟。

在**on start**积木块里，设置了两个变量，变量**f**为声音的频率，变量**item**为频率变化的间隔。

![](https://i.imgur.com/Jwr97SA.jpg)

在**forever**积木块里，**analog write pin P0 to 512**表示让P0口输出方波。

![](https://i.imgur.com/40bHXlV.jpg)

变量**T**为方波的周期，我们都知道周期=1秒/频率，在**Analog Set Period**中时间是以us为单位计量的，所以**T=1000000/f**。 

![](https://i.imgur.com/uIUqFVh.jpg)

每一次循环，都让频率**f**变为**item**，频率**f**在20Hz到6000Hz范围内来回循环。

![](https://i.imgur.com/TNh0ZHb.jpg)


## 实验结果  
---

蜂鸣器发出的声响在低频与高频间来回循环，并且把频率以柱形图的形式显示在micro：bit屏幕上。

![](https://i.imgur.com/2AJXtVY.gif)


## 思考  
---

如果我们想用温度传感器与蜂鸣器做一个高温报警器，那么我们该如何设计电路与编程？欢迎来与我们讨论。


## 常见问题
---


## 相关阅读  
---

[Micro:bit小小科学家课程01:LED](/Micro_bit_Starter_Kit_Lesson_01_LED_CN/)                       
[Micro:bit小小科学家课程02:按钮](/Micro_bit_Starter_Kit_Lesson_02_Button_CN/)  
[Micro:bit小小科学家课程03:电位器](/Micro_bit_Starter_Kit_Lesson_03_Trimpot_CN/)  
[Micro:bit小小科学家课程04:光敏电阻](/Micro_bit_Starter_Kit_Lesson_04_Photocell_CN/)  
[Micro:bit小小科学家课程05:三色LED](/Micro_bit_Starter_Kit_Lesson_05_RGB_LED_CN/)  
[Micro:bit小小科学家课程06:自锁开关](/Micro_bit_Starter_Kit_Lesson_06_Self_lock_Switch_CN/)  
[Micro:bit小小科学家课程07:温度传感器](/Micro_bit_Starter_Kit_Lesson_07_Temperature_Sensor_CN/)  
[Micro:bit小小科学家课程08:舵机](/Micro_bit_Starter_Kit_Lesson_08_Servo_CN/)  
[Micro:bit小小科学家课程10:电机](/Micro_bit_Starter_Kit_Lesson_10_Motor_CN/)  
[Micro:bit小小科学家课程11:七彩灯环](/Micro_bit_Starter_Kit_Lesson_11_Rainbow_LED_CN/)  
[Micro:bit小小科学家课程12:加速度计](/Micro_bit_Starter_Kit_Lesson_12_Accelerometer_CN/)  
[Micro:bit小小科学家课程13:指南针](/Micro_bit_Starter_Kit_Lesson_13_Compass_CN/)  
[Micro:bit小小科学家课程14:环境光](/Micro_bit_Starter_Kit_Lesson_14_Ambient_Light_CN/)  
