![13](https://i.imgur.com/xMxllOG.jpg)  

## 介绍  
---

你知道指南针是什么吗？我相信你们很多人都曾经玩过指南针。今天，我们将用micro:bit来制作一个指南针，并在LED七彩灯环上显示方向。 想知道怎么做吗？只要阅读下面的文章，跟着我的步骤操作就可以了。让我们开始吧！  


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

**指南针**

这里，指南针实际上指的是一个磁力计。磁力计是一个单独的芯片，用于感应磁场强度。在标准运行时中的软件算法使用了板载的加速度计将这些读数转换成板子原始独立的指南针读数。在使用前，必须校准指南针。校准的过程由运行软件自动发起。这个元件通过I2C母线连接到了应用处理器上。

![](https://i.imgur.com/jWLNeqO.jpg) 

## 主要元件介绍  
---

按照下图，完成硬件的连接。
![](https://i.imgur.com/8m3Efwt.jpg)

连接完成后，实物图如下：
![](https://i.imgur.com/L5VkXKE.jpg)

注意：我们必须把灯环按照图示的方向固定，才能指向正确的方向。 


## 编程  
---

打开[MakeCode在线编辑器](https://makecode.microbit.org/)，在代码编辑区域中编写代码。建议你先自己尝试着编程。
当然，你也可以通过下面这个链接下载程序的完整代码。点击右上角的“编辑”，然后再点击右下角的“下载”，你就可以将代码直接下载到micro:bit上了。
程序完整代码的链接：[https://makecode.microbit.org/_Xah0mih6PYTg](https://makecode.microbit.org/_Xah0mih6PYTg)

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_Xah0mih6PYTg" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>


## 代码解释  
---

**Compass Heading**

找到micro:bit指南针指向的方向。
micro:bit用它内置的磁力计芯片测量从0度到360度的指南针朝向。不同的数字分别代表了东西南北四个方向。0度代表正北。
LED七彩灯环带有8颗灯珠。这些灯珠分别代表了8个方位：正北、东北、正东、东南、正南、西南、正西、西北。

![](https://i.imgur.com/30chQqn.jpg) 

我们将这个360度的坐标轴系统平均分为8个区域，来帮助我们判断指南针朝向的输出数值。当数值到达了一个区域，就意味着micro:bit指向那个区域所显示的方向。  

![](https://i.imgur.com/jWkhSSr.jpg)

这个函数将对角线上的2个像素点分别设置成红色和蓝色，而其他的LED灯则不点亮。我们用红色代表正北，蓝色代表正南，以及RGB0色值来代表熄灭LED灯珠。   
转动micro:bit, 方向指向将会发生变化。但是，我们需要让LED彩虹灯始终指向同一方向。因此，我们必须使LED彩虹灯的灯珠转向相反的方向。这里，我们用**rotate pixels**来设置LED彩虹灯环的偏移量。

![](https://i.imgur.com/IOhwt7b.jpg)

这个程序的关键点在于判断**Compass Heading**的输出数值出现在哪个区域，并朝相反的方向偏移灯环色值。虽然整个程序看起来非常长，但是实际上大部分都是非常相似的。它非常简单。你可以自己编程哦！ 


## 实验结果  
---

旋转整个装置，你可以看到LED七彩灯环始终指向同一个方向。
注意：每次当你开始用指南针的时候（例如：如果你刚好启动了micro:bit),micro:bit将会开始校准指南针（自我调整）。倾斜micro:bit,它就会要求你画一个圆。
如果你正在校准或者在金属附近使用指南针，这有可能会使micro:bit的方向感应出错。

![](https://i.imgur.com/HI0MDIB.gif)


## 思考   
---

如果这个指南针案例不用灯环，直接在micro:bit的屏幕上用箭头来做指示，该如何设计电路与编程？欢迎来与我们讨论。


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
[Micro:bit小小科学家课程14:环境光](/Micro_bit_Starter_Kit_Lesson_14_Ambient_Light_CN/)           


## 更多信息，欢迎访问：
---
[micro:bit知识库地址](https://www.elecfreaks.com/learn-cn/)    
micro:bit官方推荐供应商：[恩孚科技淘宝店](https://shop69086944.taobao.com/?spm=a230r.7195193.1997079397.2.RSthR0)  
QQ技术交流群：570756726   
