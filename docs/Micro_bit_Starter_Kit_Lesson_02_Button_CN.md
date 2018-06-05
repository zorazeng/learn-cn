![2](https://i.imgur.com/SVbSfPB.jpg)

## 介绍:
---

在上一个实验中，我们已经学习了如何让micro:bit控制2颗LED灯交替闪烁。这次我们将使用一个按钮来控制LED灯的闪烁。当我们按下按钮，2颗LED灯会交替闪烁；松开按钮，LED灯就会停止闪烁。


## 元件清单：
---

### 硬件：

- 1 x [micro:bit](http://www.elecfreaks.com/estore/bbc-micro-bit-board-for-coding-programming.html)  
- 1 x USB线  
- 1 x [micro:bit面包板扩展板](http://www.elecfreaks.com/estore/microbit-breadboard-adapter.html)  
- 1 x [面包板83x55 mm](http://www.elecfreaks.com/estore/transparent-breadboard-83-55-mm.html)  
- 2 x LED  
- 2 x 100欧姆电阻  
- 1 x 瞬时按钮开关  
- 1 x [跳线](http://www.elecfreaks.com/estore/breadborad-jumper-wire-65pcs-pack.html)  

**温馨提示：如果你需要以上所有元件，你可以购买我们的[Elecfreaks小小科学家套件](https://item.taobao.com/item.htm?spm=a1z10.1-c-s.w4024-17803785896.2.18dc3f94XOgpWg&id=562837851877&scene=taobao_shop)。**

![](https://i.imgur.com/W4tseua.jpg)

### 软件：

[微软Makecode在线编辑器](https://makecode.microbit.org/)


## 主要元件介绍
---

### 瞬时按钮开关

这是一个用来控制电子设备的普通元件。它大部分用于连接或者切断控制电路，从而实现电机或者其他电子设备的控制。
瞬时按钮开关通常是保持开启的。当它被按下的时候，电路就接通了；当它被弹起的时候，它就会跳回到未连接的状态。

![](https://i.imgur.com/IO2KzaW.jpg)

瞬时按钮开关有4个引脚。这4个引脚可以被分为2组：引脚1短接引脚2，引脚3短接引脚4。

![](https://i.imgur.com/OgWZfBQ.jpg)


## 硬件连接
---

按照下面的图片，将你的元件连接。

![](https://i.imgur.com/qXKoSN4.jpg) 

这是连接完成后的样子：

![](https://i.imgur.com/uGLigLh.jpg)


## 编程
---

打开[Makecode在线编辑器](https://makecode.microbit.org/)，在代码编辑区域编写你的代码。建议你先自己尝试着去编程。 

当然，你也可以通过下面这个链接下载程序的完整代码。只要点击右上角的“编辑”，然后再点击右下角的“下载”，将程序下载到micro:bit上。

<div style="position:relative;height:0;padding-bottom:81.97%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/---run?id=_6sjLfwXVhaxg" allowfullscreen="allowfullscreen" sandbox="allow-popups allow-forms allow-scripts allow-same-origin" frameborder="0"></iframe></div>


## 代码解释：
---

**on start**

在程序开始的时候运行的一个事件。
on start是一个特殊的事件。它在程序开始的时候运行，并位于其他任何事件的前面。用这个事件来初始化你的程序。

**set pull**

设置指定引脚的电拉力。
很多micro:bit引脚都可以被设置成上拉模式。例如：一个上拉模式可以将一个引脚的电压设置成高电压（3.3V或者1V，当调用digital read pin积木块的时候)。如果按钮的一端连接到了P0（设置成高电压），另一端连接到了GND (0V),那么当你按下按钮，P0被0V驱动，micro:bit软件就检测到一个按钮被按下。

**if**

If开启了一个条件判断语句。当if后面的表达是true（或1），那么运行它里面的程序。当if后面的表达是false（或0），它将会跳出程序的循环。下面是If语句的结构： 

![](https://i.imgur.com/IrqTK6y.jpg)

**digital read**

Digital read主要是读取引脚的电压。当它读出高电压，它就会显示1.当它读出低电压，它就显示0。


## 实验结果：

当你按下按钮，你可以看到2颗LED灯交替闪烁；松开按钮，这两颗LED灯就停止闪烁。

![](https://i.imgur.com/7w5yp6z.gif)


## 思考：

如果我们想按下按钮点亮红色的LED灯，松开按钮点亮绿色的LED等，那么我们该如何编程呢？欢迎给我们留言或者和我们进一步探讨。


## 常见问题
---


## 相关阅读：
---

[Micro:bit小小科学家课程01:LED](/Micro_bit_Starter_Kit_Lesson_01_LED_CN/)  
[Micro:bit小小科学家课程03:电位器](/Micro_bit_Starter_Kit_Lesson_03_Trimpot_CN/)  
[Micro:bit小小科学家课程04:光敏电阻](/Micro_bit_Starter_Kit_Lesson_04_Photocell_CN/)  
[Micro:bit小小科学家课程05:三色LED](/Micro_bit_Starter_Kit_Lesson_05_RGB_LED_CN/)  
[Micro:bit小小科学家课程06:自锁开关](/Micro_bit_Starter_Kit_Lesson_06_Self_lock_Switch_CN/)  
[Micro:bit小小科学家课程07:温度传感器](/Micro_bit_Starter_Kit_Lesson_07_Temperature_Sensor_CN/)  
[Micro:bit小小科学家课程08:舵机](/Micro_bit_Starter_Kit_Lesson_08_Servo_CN/)  
[Micro:bit小小科学家课程09:蜂鸣器](/Micro_bit_Starter_Kit_Lesson_09_Buzzer_CN/)  
[Micro:bit小小科学家课程10:电机](/Micro_bit_Starter_Kit_Lesson_10_Motor_CN/)  
[Micro:bit小小科学家课程11:七彩灯环](/Micro_bit_Starter_Kit_Lesson_11_Rainbow_LED_CN/)  
[Micro:bit小小科学家课程12:加速度计](/Micro_bit_Starter_Kit_Lesson_12_Accelerometer_CN/)  
[Micro:bit小小科学家课程13:指南针](/Micro_bit_Starter_Kit_Lesson_13_Compass_CN/)  
[Micro:bit小小科学家课程14:环境光](/Micro_bit_Starter_Kit_Lesson_14_Ambient_Light_CN/)  


