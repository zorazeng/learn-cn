![5](https://i.imgur.com/mEAx3Tx.jpg)  

## 介绍
---

三色LED是LED灯的一种。它能够发出红、绿、蓝三种不同颜色的光线。在本次实验中，我们将让RGB LED在红、绿、蓝三种颜色之间渐变转换。


## 元件清单  
---

### 硬件：

- 1 x [micro:bit](http://www.elecfreaks.com/estore/bbc-micro-bit-board-for-coding-programming.html)
- 1 x USB线
- 1 x [microbit面包板扩展板](http://www.elecfreaks.com/estore/microbit-breadboard-adapter.html)
- 1 x [面包板83 x 55 mm](http://www.elecfreaks.com/estore/transparent-breadboard-83-55-mm.html)
- 1 x RGB LED
- 3 x 100欧姆电阻
- 1 x [跳线](http://www.elecfreaks.com/estore/breadborad-jumper-wire-65pcs-pack.html)

**温馨提示：如果你需要以上所有元件，你可以购买我们的[Elecfreaks小小科学家套件](https://item.taobao.com/item.htm?spm=a1z10.1-c-s.w4024-17803785896.2.18dc3f94XOgpWg&id=562837851877&scene=taobao_shop)。**

![](https://i.imgur.com/W4tseua.jpg)

### 软件：

[微软MakeCode在线编辑器](https://makecode.microbit.org/)


## 主要元件介绍  
---

#### 三色LED

三色LED是LED的一种，把红色LED、绿色LED、蓝色LED集合成一个元件，就是RGB LED。我们都知道，光的三原色分别为红色、绿色、蓝色，利用这三种颜色进行不同组份地组合，能够合成出万物所有的颜色。同样，利用RGB LED进行不同亮度的组合，能够形成无数种颜色。  

![](https://i.imgur.com/9VLb4LB.jpg)
![](https://i.imgur.com/kaoHHJ2.jpg)
  
三色LED分为两种类型，分别为共阴极与共阳极：共阴极的RGB LED公共端接GND；共阳极的RGB LED公共端接VCC。在本实验中，我们选用共阴极的三色LED。 

## 硬件连接  
---

请按照下图完成硬件的连接。

![](https://i.imgur.com/krrGHBs.jpg)

连线完成后，实物图如下：  

![](https://i.imgur.com/DkfsnTs.jpg)


## 编程  
---

打开[MakeCode在线编辑器](https://makecode.microbit.org/)，在代码编辑区域编写代码。建议你先自己尝试着编程。  

当然，你也可以通过在下面这个链接下载程序的完整代码。点击右上角的“编辑”，然后再点击右下角的“下载”，你就可以将代码直接下载到micro:bit上了。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_7PJd01g8pc8i" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>


## 代码解释  
---

**Change Value**

设置本地变量和全局变量的数值。通过1来改变r等同于“r=r+1”。

**repeat**

按照指定次数运行部分程序。

**function**

函数是一些可以在程序中重用的代码。 你可以用一个函数定义来创建一个函数。函数定义指的是给函数命名并指定它的代码。函数调用是在程序的某处通过使用函数的名称来引用这个函数。

**call function**

在程序的某处通过使用函数的名称来引用这个函数。

![](https://i.imgur.com/6dB22J0.jpg)

在这个实验中，我们设置了r、g 、b三个变量，分别用来记录红、绿、蓝这三种颜色的亮度。在初始状态下，只发出红光。

![](https://i.imgur.com/tWiLbVy.jpg)

接着，我们需要创建3个函数来实现这三种颜色的渐变。
例如：红色到绿色渐变的函数“RtoG”。函数内的循环每执行1次，P0口的模拟输入就-1（红色亮度降低一点）；P1口的模拟输入就+1（绿色亮度就升高一点）。循环1023次后，P0口模拟输入为0（红色熄灭），P1口模拟输入为1023（绿灯最亮），从而实现了平滑的渐变过渡。

![](https://i.imgur.com/DFZWDN5.jpg)

循环调用这三个函数，实现3种颜色的均匀过渡。


## 实验结果  
---

按下按钮A，LED发出红光。 
按下按钮B，LED发出绿光。
同时按下按钮A和B， LED发出蓝光。


## 思考  
---

如果想要用三色LED发出青色、品红色、黄色的光线，该如何设计电路与编程？欢迎来与我们讨论。 


## 常见问题
---


## 相关阅读  
---

[Micro:bit小小科学家课程01:LED](/Micro_bit_Starter_Kit_Lesson_01_LED_CN/)                     
[Micro:bit小小科学家课程02:按钮](/Micro_bit_Starter_Kit_Lesson_02_Button_CN/)
[Micro:bit小小科学家课程03:电位器](/Micro_bit_Starter_Kit_Lesson_03_Trimpot_CN/)
[Micro:bit小小科学家课程04:光敏电阻](/Micro_bit_Starter_Kit_Lesson_04_Photocell_CN/)
[Micro:bit小小科学家课程06:自锁开关](/Micro_bit_Starter_Kit_Lesson_06_Self_lock_Switch_CN/)
[Micro:bit小小科学家课程07:温度传感器](/Micro_bit_Starter_Kit_Lesson_07_Temperature_Sensor_CN/)
[Micro:bit小小科学家课程08:舵机](/Micro_bit_Starter_Kit_Lesson_08_Servo_CN/)
[Micro:bit小小科学家课程09:蜂鸣器](/Micro_bit_Starter_Kit_Lesson_09_Buzzer_CN/)
[Micro:bit小小科学家课程10:电机](/Micro_bit_Starter_Kit_Lesson_10_Motor_CN/)
[Micro:bit小小科学家课程11:七彩灯环](/Micro_bit_Starter_Kit_Lesson_11_Rainbow_LED_CN/)
[Micro:bit小小科学家课程12:加速度计](/Micro_bit_Starter_Kit_Lesson_12_Accelerometer_CN/)
[Micro:bit小小科学家课程13:指南针](/Micro_bit_Starter_Kit_Lesson_13_Compass_CN/)
[Micro:bit小小科学家课程14:环境光](/Micro_bit_Starter_Kit_Lesson_14_Ambient_Light_CN/)

