![14](https://i.imgur.com/NkZTTdv.jpg)  
## 介绍  
---

在光敏传感器这个实验里，我们外接一个光敏传感器来感知外界光线，实际上，在micro:bit内部，也集成了一个光敏感应装置，本次实验，我们就用内部集成的光敏感应装置。当外界环境光比较暗时，点亮灯环。  


## 元件清单  
---

### 硬件:

- 1 x micro:bit
- 1 x USB线
- 1 x micro:bit面包板扩展板
- 1 x 面包板83 x 55 mm
- 1 x LED七彩灯环（8颗灯珠）
- 1 x 跳线

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

程序完整代码的链接：[https://makecode.microbit.org/_hYgejm37CVLi](https://makecode.microbit.org/_hYgejm37CVLi)
<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_hYgejm37CVLi" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>


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

[Micro:bit小小科学家课程01:LED](/Micro_bit_Starter_Kit_Lesson_01_LED_CN/)                        
[Micro:bit小小科学家课程02:按钮](/Micro_bit_Starter_Kit_Lesson_02_Button_CN/)   
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


## 更多信息，欢迎访问：
---
[micro:bit知识库地址](https://www.elecfreaks.com/learn-cn/)    
micro:bit官方推荐供应商：[恩孚科技淘宝店](https://shop69086944.taobao.com/?spm=a230r.7195193.1997079397.2.RSthR0)  
QQ技术交流群：570756726  
