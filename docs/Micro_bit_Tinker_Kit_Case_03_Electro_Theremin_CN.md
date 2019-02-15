

![](https://i.imgur.com/TJvoaaV.jpg)

## 制作目标
---

- 学习micro:bit和电位器的使用。
- 学习制作一个电子琴。


## 所需材料
---
 
- 1 x [BBC micro:bit](http://www.elecfreaks.com/estore/bbc-micro-bit-board-for-coding-programming.html)
- 1 x USB线
- 1 x [蜂鸣器模块](http://www.elecfreaks.com/estore/octopus-passive-buzzer-brick-obpb01.html)
- 1 x [电位器模块](http://www.elecfreaks.com/estore/octopus-analog-rotation-brick-obarot.html)
- 1 x [扩展板](http://www.elecfreaks.com/estore/elecfreaks-micro-bit-breakout-board.html)

**温馨提示: 如果你想要以上所有这些元器件，你可以购买我们的[micro:bit小小发明家套件](https://item.taobao.com/item.htm?spm=a230r.7195193.1997079397.9.z3IMPf&id=564707672256&abbucket=5)。**


## 制作过程
---

### 步骤1

将蜂鸣器模块插入扩展板上的P0。确保正极插入扩展板上的黄色信号引脚，负极插入黑色接地引脚。
将电位器模块插入P1。确保线的颜色和扩展板上引脚的颜色一致。

![](https://i.imgur.com/zSbp5LP.jpg)


### 步骤2

在MakeCode中，我们将用一个变量来追踪电位器的值。变量就像水桶一样可以装载这些不断变化的数值。
在变量选择区域，创建一个新的变量命名为reading (或者是你喜欢的其他名称)。
我们想要把这个reading的变量设置为电位器的模拟值，而不仅仅是数字。
读取电位器的模拟值可以让我们从电位器上获得一系列信号，而不仅仅是数字0和1。在Pins抽屉里面找到下面这个积木块。

![](https://i.imgur.com/xS411pj.png)


### 步骤3  

通过展示变量reading的读数来获取电位器的最大值和最小值。
逆时针旋转电位器的旋钮，你将会得到最小值；顺时针旋转则会获得最大值。
你发现了数值是如何变动的吗？那是因为micro:bit需要一点时间来在屏幕上显示一串数字。之后，你就会看到一个新的数值。电位器的数值可能在最前面哦！ 

![](https://i.imgur.com/N94OcoS.png)


### 步骤4  

现在我们要开始用你刚刚读取的电位器的数值来制作音符。音乐积木块的音符不像电位器的数值一样广泛。因此，我们想让电位器的最大值与音调最高的音符对应。
在MakeCode的piano按键中找到最高的音符和最低的音符。
使用MakeCode代码选择区域的map积木块来编辑所有的值。 

![](https://i.imgur.com/pvXNEQ3.png)


### 步骤5  

你可能注意到上一步我们创建了一个新的变量，叫做note。把变量note设置为映射的数值。使用变量note让音乐响起。然后把所有代码下载到你的micro:bit上，你就可以听到声音啦！

![](https://i.imgur.com/2NiVA0B.jpg)

如果你不想自己动手编写这些代码的话，你可以从下面这个链接下载程序的完整代码：

[https://makecode.microbit.org/_bK4T5Kh4qarH](https://makecode.microbit.org/_bK4T5Kh4qarH)

或者，你也可以从下面这个页面下载代码：

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_bK4T5Kh4qarH" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>


### 太棒啦！  

现在你已经学会了如何用电位器来播放音乐。你可以尝试着控制LED，舵机以及其他的元件。 如果你用了其他的模拟传感器，你就会明白怎样使用了！


## 常见问题
---


## 相关阅读  
---

[Micro:bit小小发明家课程01:音乐播放器](/Micro_bit_Tinker_Kit_Case_01_Music_Machine_CN/)                       
[Micro:bit小小发明家课程02:智能灯](/Micro_bit_Tinker_Kit_Case_02_Smart_Light_CN/)  
[Micro:bit小小发明家课程04:报警装置](/Micro_bit_Tinker_Kit_Case_04_Simple_Alarm_Box_CN/)  
[Micro:bit小小发明家课程05:土壤湿度检测](/Micro_bit_Tinker_Kit_Case_05_Plant_Monitoring_Device_CN/)  
[Micro:bit小小发明家课程06:入侵检测](/Micro_bit_Tinker_Kit_Case_06_Intruder_Detection_CN/)  
[Micro:bit小小发明家课程07:喂鱼器](/Micro_bit_Tinker_Kit_Case_07_Fish_Feeder_CN/)  
[Micro:bit小小发明家课程08:运动检测](/Micro_bit_Tinker_Kit_Case_08_Motion_Detector_CN/)  
[Micro:bit小小发明家课程09:测谎仪](/Micro_bit_Tinker_Kit_Case_09_Lie_Detector_CN/)  
[Micro:bit小小发明家课程10:乒乓球游戏](/Micro_bit_Tinker_Kit_Case_10_PADDLEBALLSUPERSMASHEM_CN/)  
[Micro:bit小小发明家课程11:躲避小行星](/Micro_bit_Tinker_Kit_Case_11_Avoid_Asteroids_CN/)  
[Micro:bit小小发明家课程12:遥控小车](/Micro_bit_Tinker_Kit_Case_12_Remote_Control_Everything_CN/)  
[Micro:bit小小发明家课程13:micro:bit小车](/Micro_bit_Tinker_Kit_Case_13_Micro_Bit_Car_CN/)  
[Micro:bit小小发明家课程14:抛煎饼游戏](/Micro_bit_Tinker_Kit_Case_14_Flipping_Pancakes_CN/)  
[Micro:bit小小发明家课程15:跑迷宫游戏](/Micro_bit_Tinker_Kit_Case_15_Maze_Runner_CN/)  
[Micro:bit小小发明家课程16:速算游戏](/Micro_bit_Tinker_Kit_Case_16_QUICK_MATHS_CN/)  
[Micro:bit小小发明家课程17:猜音调游戏](/Micro_bit_Tinker_Kit_Case_17_Pitch_Perfect_CN/)  
[Micro:bit小小发明家课程18:手指灵敏度游戏](/Micro_bit_Tinker_Kit_Case_18_Finger_Dexterity_CN/)  
[Micro:bit小小发明家课程19:电子水平仪](/Micro_bit_Tinker_Kit_Case_19_Electric_Spirit_Level_CN/)  
[Micro:bit小小发明家课程20:太空射击游戏](/Micro_bit_Tinker_Kit_Case_20_Space_Shooter_CN/)  
[Micro:bit小小发明家课程21:飞行的小鸟游戏](/Micro_bit_Tinker_Kit_Case_21_Flappy_Bird_CN/)  
[Micro:bit小小发明家课程22:摩尔斯代码信息传输](/Micro_bit_Tinker_Kit_Case_22_Wire_Transmission_CN/)  
[Micro:bit小小发明家课程23:贪吃蛇游戏](/Micro_bit_Tinker_Kit_Case_23_Snake_Game_CN/)  
