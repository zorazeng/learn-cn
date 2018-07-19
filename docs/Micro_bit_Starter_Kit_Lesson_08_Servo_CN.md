![8](https://i.imgur.com/DuxosEs.jpg)

## 介绍  
---

舵机是一种位置（角度）伺服的驱动器，适用于那些需要角度不断变化并可以保持的控制系统。在这次的实验中，我们将用micro:bit控制舵机在行程范围内循环转动。


## 元件清单  
---

### 硬件:

- 1 x micro:bit
- 1 x USB线
- 1 x microbit面包板扩展板
- 1 x 面包板83 x 55 mm
- 1 x TowerPro SG-90 舵机(1.6kg)
- 1 x 跳线

**温馨提示：如果你需要以上所有元件，你可以购买我们的[Elecfreaks小小科学家套件](https://item.taobao.com/item.htm?spm=a1z10.1-c-s.w4024-17803785896.2.18dc3f94XOgpWg&id=562837851877&scene=taobao_shop)。**

![](https://i.imgur.com/W4tseua.jpg)

### 软件：

[微软MakeCode在线编辑器](https://makecode.microbit.org/)


## 主要元件介绍  
---

### 舵机  

舵机由直流电机、减速齿轮组、电位器和控制电路组成的一套自动控制系统。通过发送信号，指定输出轴旋转角度。舵机一般而言都有最大旋转角度（比如180度）。与普通直流电机的区别主要在，直流电机是一圈圈转动的，舵机只能在一定角度内转动，不能一圈圈转（数字舵机可以在舵机模式和电机模式中切换，没有这个问题）。普通直流电机无法反馈转动的角度信息，而舵机可以。用途也不同，普通直流电机一般是整圈转动做动力用，舵机是控制某物体转动一定角度用，如机器人的关节。 舵机的伺服系统由可变宽度的脉冲来进行控制，控制线是用来传送脉冲的。脉冲的参数有最小值，最大值，和频率。一般而言，舵机的基准信号都是周期为20ms，宽度为1.5ms。这个基准信号定义的位置为中间位置。舵机有最大转动角度，中间位置的定义就是从这个位置到最大角度与最小角度的量完全一样。最重要的一点是，不同舵机的最大转动角度可能不相同，但是其中间位置的脉冲宽度是一定的，那就是1.5ms。  

![](https://i.imgur.com/btuF5m0.jpg)

注意：micro:bit官方已经将舵机的控制代码封装成积木块，用Makecode编程时，无需考虑脉冲宽度之类的复杂信息。

舵机有很多规格，但所有的舵机都有外接三根线，分别用棕、红、橙三种颜色进行区分（品牌不同，颜色可能会略有差异），棕色为接地线，红色为电源正极线，橙色为信号线。  

![](https://i.imgur.com/8sQBiV7.jpg)


## 硬件连接  
---

按照下图, 完成硬件的连接。
![](https://i.imgur.com/csCETYN.jpg)

连接完成后，实物图如下：
![](https://i.imgur.com/ZaV3kW3.jpg)


## 编程  
---

打开[MakeCode在线编辑器](https://makecode.microbit.org/)，在代码编辑区域中编写代码。建议你先自己尝试着编程。

程序完整代码的链接：[https://makecode.microbit.org/_Yd7X6x1dKfgv](https://makecode.microbit.org/_Yd7X6x1dKfgv)

当然，你也可以通过下面这个页面查看程序的完整代码。点击右上角的“编辑”，然后再点击右下角的“下载”，你就可以将代码直接下载到micro:bit上了。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_Yd7X6x1dKfgv" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>


## 代码解释  
---

**Servo Write Pin**

给指定的引脚上的舵机写入一个数值，控制舵机轴的运动。
这个函数将会移动标准舵机的轴到指定的角度，或者设置舵机持续旋转的速度。（0代表在一个方向上的全速，180代表另一个方向上的全速，并且将近90度代表无运动。）


## 实验结果  
---

舵机在0至180度之间来回旋转。

![](https://i.imgur.com/baPL7VS.gif)


## 思考  

如果我们想用温度传感器和舵机做一个指针温度计，那么我们该如何设计电路与编程？欢迎来与我们讨论。


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

