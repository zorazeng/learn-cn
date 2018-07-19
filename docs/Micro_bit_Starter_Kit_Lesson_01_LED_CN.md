![1](https://i.imgur.com/GMzHtFZ.jpg)

## 简介：
---

LED灯的应用非常广泛。在日常生活中，我们看到的大部分信号灯都采用了LED灯作为它的主要光源。在今天的实验中，我们将要用micro:bit使2颗LED灯交替闪烁。 


## 元件清单：
---

### 硬件：

- 1 x micro:bit
- 1 x USB线  
- 1 x micro:bit面包板扩展板
- 1 x 面包板83x55mm 
- 2 x LED  
- 2 x 100欧姆电阻  
- 1 x 跳线

**温馨提示：如果你需要以上所有元件，你可以购买我们的[Elecfreaks小小科学家套件](https://item.taobao.com/item.htm?spm=a1z10.1-c-s.w4024-17803785896.2.18dc3f94XOgpWg&id=562837851877&scene=taobao_shop)。**

![](https://i.imgur.com/W4tseua.jpg)

### 软件：

[微软Makecode在线编辑器](https://makecode.microbit.org/)


## 主要元件介绍
---

### micro:bit面包板扩展板

micro:bit面包板扩展板可以在面包板上扩展出micro:bit的所有引脚，方便我们在面包板上制作简单的电路。

![](https://i.imgur.com/dq75zKC.jpg)
 
下面这张图片显示了如何将面包板扩展板插入到面包板上。面包板扩展板可以适用于各种规格的面包板。

![](https://i.imgur.com/3DHC6U8.jpg)

### LED

LED是Light Emitting Diode（发光二极管）的缩写。这是一种半导体二极管。它可以将电能转换成光能。当电流经过的时候，它就会发光。
 
![](https://i.imgur.com/gDwJTlH.jpg)
![](https://i.imgur.com/t8e1q6X.jpg)
 
如果你仔细看看LED，你就会发现它的两个特点。一个是它的引脚的长度不一致，另一个是LED的一侧是扁平的，而不是圆柱形。这些特征可以告诉你哪个引脚是阳极（正极），哪个引脚是阴极（负极）。长一些的引脚连接正极供电（3.3v),带有扁平一侧的引脚连接接地。

### 电阻

电阻是一种用于控制电流的元件。它可以限制所连接的电路的电流。在我们的实验中，我们使用了100欧姆的电阻。如果不限制电流的话，就会损坏LED灯。

![](https://i.imgur.com/WS9Fk9x.jpg)

想通过色环来识别电阻的阻值吗？你可以阅读这篇文章：
[How to Identify Color Circle Resistance Value](https://www.elecfreaks.com/9158.html).


## 硬件连接
---

根据下面的图片将你的元件连接起来：
![](https://i.imgur.com/6JA8ooG.jpg)

这是连接完成后的图片:
![](https://i.imgur.com/ZEP7gfe.jpg)


## 编程
---

打开[Makecode在线编辑器](https://makecode.microbit.org/)，在代码编辑区域编写以下代码。 

![](https://i.imgur.com/s5sUftj.jpg)

程序的完整代码链接：[https://makecode.microbit.org/_5mX7DsegXVJq ](https://makecode.microbit.org/_5mX7DsegXVJq )
 
你可以在下面这个页面中查看程序的完整代码。点击右上角的“编辑”，然后再点击“下载”将你的代码下载到micro:bit上。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_5mX7DsegXVJq" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>


## 代码解释：
---

**Forever**  
forever积木块可以一遍又一遍地循环插入它内部的任何其他指令的积木块，并永远循环。它从顶部开始运行代码，一直运行到底部，然后又从顶部开始运行。

**Digital Write**

DigitalWrite积木块可以让你开启或者关闭一个引脚。它有一个下拉选项，让你选择你想控制的那个引脚，并且它允许将一个变量作为引脚的状态。你可以用1来代表开启，0代表关闭。如果你想的话，你还可以使用布尔状态true和false，但是我们在这个教程中将会使用0和1来作为我们的标准。

**Pause**  
如果你只是用digital write积木块来开启或者关闭引脚而无任何停顿，LED灯可能会闪烁得非常非常快。pause积木块可以减慢micro:bit的程序运行速度，让你控制事件发生的时间。你可以用一个数字或者变量作为你想要暂停的毫秒数。你可以把它视为让代码的暂停的红灯哦！


## 实验结果
---

你可以看到两颗LED灯交替闪烁。如果不是这样的话，请返回之前的步骤，检查你的操作。

![](https://i.imgur.com/xvYjvaQ.gif)


## 思考
---

如果我们想控制4颗LED灯，让它们依次被点亮，那么我们该如何设计电路和编程呢？欢迎和我们进行进一步探讨。你可以在下方的评论区给我们留言。


## 常见问题
---


## 相关阅读
---


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
[Micro:bit小小科学家课程14:环境光](/Micro_bit_Starter_Kit_Lesson_14_Ambient_Light_CN/)    

## 更多信息，欢迎访问：
---
[micro:bit知识库地址](https://www.elecfreaks.com/learn-cn/)    
micro:bit官方推荐供应商：[恩孚科技淘宝店](https://shop69086944.taobao.com/?spm=a230r.7195193.1997079397.2.RSthR0)  
QQ技术交流群：570756726   



