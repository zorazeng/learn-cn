![6](https://i.imgur.com/ogadD6b.jpg)  

## 介绍

自锁开关，是一种常见的按钮开关。当我们初次按下开关按钮时，开关电路连接并保持这种状态，即自锁。再次按下开关按钮时，开关断开，同时开关按钮弹出来。在这次实验中，我们将使用自锁开关来控制LED的点亮与熄灭。


## 元件清单  
---

### 硬件：

- 1 x micro:bit
- 1 x USB线
- 1 x microbit面包板扩展板
- 1 x 面包板83 x 55 mm
- 1 x 自锁开关
- 1 x LED
- 1 x 100欧姆电阻
- 1 x 跳线

**温馨提示：如果你需要以上所有元件，你可以购买我们的[Elecfreaks小小科学家套件](https://item.taobao.com/item.htm?spm=a1z10.1-c-s.w4024-17803785896.2.18dc3f94XOgpWg&id=562837851877&scene=taobao_shop)。**

![](https://i.imgur.com/W4tseua.jpg)

### 软件：

[微软MakeCode在线编辑器](https://makecode.microbit.org/)


## 主要元件介绍  
---

### 自锁开关

自锁开关一般是指开关自带机械锁定功能，按下去，松手后按钮是不会完全跳起来的，处于锁定状态，需要再按一次，才解锁完全跳起来。它就叫自锁开关。早期的直接完全断电的电视机、显示器就是使用的这种类型的开关。

![](https://i.imgur.com/hareBrE.jpg)

注意：这种自锁开关包含两组刀双掷开关，本次试验只用到了其中一组，故剪去了其中一组的公共引脚。


## 硬件连接  
---

按照下图,完成硬件的连接。
![](https://i.imgur.com/k4dfMBY.jpg)

连线完成后，实物图如下：
![](https://i.imgur.com/AuCiJU3.jpg)


## 编程  
---

打开[MakeCode在线编辑器](https://makecode.microbit.org/)，在代码编辑区域中编写代码。建议你先自己尝试着编程。

程序完整代码的链接：[https://makecode.microbit.org/_7HuKC72t1DVi](https://makecode.microbit.org/_7HuKC72t1DVi)

当然，你也可以通过下面这个页面查看程序的完整代码。点击右上角的“编辑”，然后再点击右下角的“下载”，你就可以将代码直接下载到micro:bit上了。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_2UHaYkMfpKc6" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>


## 代码解释  
---

**set events** 
配置给定引脚发出的事件类型。

**on events **
在事件集合区域发起一个事件。
![](https://i.imgur.com/N7n6INc.jpg)

在这个案例中，我们设计了2个事件：P0电压的上升和下降。每次按下按钮的时候，P0口的电压就会改变一次。当电压开始从0V切换到3.3V的时候，我们把它叫做“上升沿”。当电压从3.3V开始切换到0V时，我们把它叫做“下降沿”。

![](https://i.imgur.com/kcnveNe.jpg)


## 实验结果
---

按下自锁开关，LED点亮；再按一次，LED熄灭。
![](https://i.imgur.com/sCMwXXf.gif)


## 思考
---

楼梯灯通常就是用单刀双掷开关来实现的，可以在楼上开灯楼下关灯，也可以在楼下开灯，去楼上关灯，如果我想用两只自锁按钮实现楼梯灯的功能，该如何设计电路与编程？欢迎来与我们讨论。


## 常见问题
---


## 相关阅读
---

[Micro:bit小小科学家课程01:LED](/Micro_bit_Starter_Kit_Lesson_01_LED_CN/)                        
[Micro:bit小小科学家课程02:按钮](/Micro_bit_Starter_Kit_Lesson_02_Button_CN/)   
[Micro:bit小小科学家课程03:电位器](/Micro_bit_Starter_Kit_Lesson_03_Trimpot_CN/)   
[Micro:bit小小科学家课程04:光敏电阻](/Micro_bit_Starter_Kit_Lesson_04_Photocell_CN/)   
[Micro:bit小小科学家课程05:三色LED](/Micro_bit_Starter_Kit_Lesson_05_RGB_LED_CN/)   
[Micro:bit小小科学家课程07:温度传感器](/Micro_bit_Starter_Kit_Lesson_07_Temperature_Sensor_CN/)   
[Micro:bit小小科学家课程08:舵机](/Micro_bit_Starter_Kit_Lesson_08_Servo_CN/)   
[Micro:bit小小科学家课程09:蜂鸣器](/Micro_bit_Starter_Kit_Lesson_09_Buzzer_CN/)   
[Micro:bit小小科学家课程10:电机](/Micro_bit_Starter_Kit_Lesson_10_Motor_CN/)   
[Micro:bit小小科学家课程11:七彩灯环](/Micro_bit_Starter_Kit_Lesson_11_Rainbow_LED_CN/)   
[Micro:bit小小科学家课程12:加速度计](/Micro_bit_Starter_Kit_Lesson_12_Accelerometer_CN/)   
[Micro:bit小小科学家课程13:指南针](/Micro_bit_Starter_Kit_Lesson_13_Compass_CN/)   
[Micro:bit小小科学家课程14:环境光](/Micro_bit_Starter_Kit_Lesson_14_Ambient_Light_CN/)   


## 更多信息，欢迎访问：
---
[micro:bit知识库地址](https://www.elecfreaks.com/learn-cn/)       
micro:bit官方推荐供应商：[恩孚科技淘宝店](https://shop69086944.taobao.com/?spm=a230r.7195193.1997079397.2.RSthR0)     
QQ技术交流群：570756726     
