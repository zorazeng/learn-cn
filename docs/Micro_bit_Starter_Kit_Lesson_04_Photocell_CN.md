![4](https://i.imgur.com/MwngMAi.jpg)

## 介绍  
---

光敏电阻是一种基于内光电效应的特殊电阻，光线越强阻值就越低，光控开关通常就是以光敏电阻为核心元件。本次实验，我们通过光敏电阻来控制micro:bit5*5LED屏幕的亮度。


## 元件清单  
---

### 硬件:  

- 1 x [micro:bit](http://www.elecfreaks.com/estore/bbc-micro-bit-board-for-coding-programming.html)
- 1 x USB线
- 1 x [micro:bit面包板扩展板](http://www.elecfreaks.com/estore/microbit-breadboard-adapter.html)
- 1 x [面包板83 x 55 mm](http://www.elecfreaks.com/estore/transparent-breadboard-83-55-mm.html)
- 1 x 光敏电阻
- 1 x 10k欧姆电阻
- 1 x [跳线](http://www.elecfreaks.com/estore/breadborad-jumper-wire-65pcs-pack.html)

**温馨提示：如果你需要以上所有元件，你可以购买我们的[Elecfreaks小小科学家套件](https://item.taobao.com/item.htm?spm=a1z10.1-c-s.w4024-17803785896.2.18dc3f94XOgpWg&id=562837851877&scene=taobao_shop)。**


![](https://i.imgur.com/W4tseua.jpg)

### 软件：  

[微软Makecode在线编辑器](https://makecode.microbit.org/)


## 主要元件介绍  
---

### 光敏电阻

光敏电阻是用CdS或CdSe等半导体材料制成的特殊电阻器，其工作原理是基于内光电效应。光照愈强，阻值就愈低，随着光照强度的升高，电阻值迅速降低，亮电阻值可小至1KΩ以下。光敏电阻对光线十分敏感，其在无光照时，呈高阻状态，暗电阻一般可达1.5MΩ。  

![](https://i.imgur.com/jS03zGQ.jpg)


## 硬件连接  
---

按照下图，完成硬件的连接。

![](https://i.imgur.com/FtQDhiS.jpg)

光敏电阻与10K欧姆电阻串联，形成一个分压电路。

连接完成后，实物图如下：

![](https://i.imgur.com/TMd3Fq8.jpg)


## 编程  
---

打开[MakeCode在线编辑器](https://makecode.microbit.org/)，在代码编辑区域编写你的代码。建议你先自己尝试着去编程。

当然，你也可以通过下面这个链接下载程序的完整代码。只要点击右上角的“编辑”，然后再点击右下角的“下载”，你就可以将程序下载到你的micro:bit中。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_K8xitbM9LPMk" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>


## 代码解释：
---

**set**

这是一个赋值运算。将a设置为1等同于“a=1”。我们用一个等号来使一个变量存储你指定的数字或字符串。
当你用这个等号在一个变量里面存储东西时，这个等号就叫做赋值运算符，而你所存储的东西就叫做数值。

**analog read**

读取你指定引脚的模拟信号（0~1023）。

**show icon**

在LED屏幕上显示所选图标。

**Clear Screen**

关闭LED屏幕上的所有LED灯。

**If else**

在实验2中，我们已经介绍了if语句的用法。在if else语句中，当表达式的值为false（或者为0）时，将执行完else积木块内的程序后执行后续程序，它的流程图如下：

![](https://i.imgur.com/E5Xi2Uu.jpg)

在这个实验中，micro:bit将P0口读取的模拟电压作为亮度的参考值。

![](https://i.imgur.com/Tck85NO.jpg)

在forever程序块中，循环扫描P0口的模拟电压。一旦当前电压值低于基准值减去2（表示光照强度变低，光敏电阻阻值下降），就说明已经关灯。 

![](https://i.imgur.com/K8tmDxV.jpg)

在程序中，calibrationVal-2其实是在调节感应灵敏度，数值越小灵敏度越高，它并不适用于所有的光照环境，你应当调节此参数，直到适应当下的光照情况。


## 实验结果  
---

开灯时，micro:bit的LED屏幕上什么都不显示；而关灯后，屏幕上显示了一个爱心图标。

![](https://i.imgur.com/1Xu4lBR.gif)

**注意：**
microbit启动后，会按照当下的亮度情况设置基准值，所以我们必须在开灯的情况下启动micro:bit程序才能正常工作。


## 思考  
---

如果想要用光敏电阻来控制一颗LED的开与关，那么我们该如何设计电路与编程？欢迎来与我们讨论。


## 常见问题
---


## 相关阅读  
---

[Micro:bit小小科学家课程01:LED](/Micro_bit_Starter_Kit_Lesson_01_LED_CN/)              
[Micro:bit小小科学家课程02:按钮](/Micro_bit_Starter_Kit_Lesson_02_Button_CN/)
[Micro:bit小小科学家课程03:电位器](/Micro_bit_Starter_Kit_Lesson_03_Trimpot_CN/)
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

