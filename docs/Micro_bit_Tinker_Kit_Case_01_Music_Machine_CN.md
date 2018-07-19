

![](https://i.imgur.com/cqLH6Bs.jpg)  

## 目标
---

• 了解ADKeypad的使用方法。
• 用ADKeypad和蜂鸣器模块制作一个小装置。


## 所需材料
---

- 1 x [BBC Micro:bit Board](http://www.elecfreaks.com/estore/bbc-micro-bit-board-for-coding-programming.html)
- 1 x USB线
- 1 x [Micro:bit扩展板](http://www.elecfreaks.com/estore/elecfreaks-micro-bit-breakout-board.html)
- 1 x [无源蜂鸣器模块](http://www.elecfreaks.com/estore/octopus-passive-buzzer-brick-obpb01.html)
- 1 x [ADKeypad](http://www.elecfreaks.com/estore/octopus-adkeypad.html)

![](https://i.imgur.com/5BURByd.jpg)

**温馨提示: 如果你想要以上所有这些元器件，你可以购买我们的[micro:bit小小发明家套件](https://item.taobao.com/item.htm?spm=a230r.7195193.1997079397.9.z3IMPf&id=564707672256&abbucket=5)。**


## 制作过程
---

### 步骤 1  

如图所示，将USB线的一端连接电脑，另一端连接micro:bit。然后把micro:bit插入扩展板。 

![](https://i.imgur.com/LZR0LH8.jpg)


### 步骤 2  

将蜂鸣器模块插入扩展板上的引脚P0。
将ADKepad插入扩展板上的引脚P2。
确保蜂鸣器和ADKeypad的接线颜色和扩展板上引脚的颜色一致。 
 
![](https://i.imgur.com/9MsaKEF.jpg)


### 步骤 3  

在MakeCode的代码抽屉中点击Advanced，查看更多代码选项。

![](https://i.imgur.com/R5lx5Np.jpg)

为了给套件中的ADKeypad和蜂鸣器模块编程，我们需要添加一个代码库。在代码抽屉底部找到“Add Package”，并点击它。这时会弹出一个对话框。搜索“tinker kit"，然后点击下载这个代码库。

![](https://i.imgur.com/pduH11r.png)

注意：如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。


### 步骤 4  

接下来，让我们一起来创建图中所示的一个条件语句。这个“if-then”积木块位于MakeCode代码抽屉中“logic”的项下。下面所示的代码的意思是：在ADKeypad被插入扩展板上的引脚P2的情况下，当我们按下ADKeypad上的A按钮，蜂鸣器将会发出175赫兹的声音。

![](https://i.imgur.com/flXdhMM.png)
 
因为ADKeypad上有5个按钮，所以我们需要编辑5个类似的条件语句。每个按钮控制一种指定的音调。因此按下不同的按钮，我们就能得到不同音调的音乐。

![](https://i.imgur.com/vHKhOqU.png)

如果你不想自己动手编写这些代码的话，你可以从下面这个链接下载程序的完整代码：

[https://makecode.microbit.org/_3VaHYtgxqRb9](https://makecode.microbit.org/_3VaHYtgxqRb9)

或者，你也可以从下面这个页面下载代码：

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_3VaHYtgxqRb9" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>

终于完成啦!现在你已经拥有了一个属于你的micro:bit音乐播放器了哦！

## 常见问题
---


## 相关阅读  
---
                   
[Micro:bit小小发明家课程02:智能灯](/Micro_bit_Tinker_Kit_Case_02_Smart_Light_CN/)  
[Micro:bit小小发明家课程03:电子琴](/Micro_bit_Tinker_Kit_Case_03_Electro_Theremin_CN/)  
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
