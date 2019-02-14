
在这个项目中，我们将用micro:bit、蜂鸣器、OLED以及湿度传感器来制作一个植物土壤湿度检测装置。当土壤水分不足时，蜂鸣器就会响起，OLED屏幕上会显示湿度的信息。


## 目标:  
---

- 1. 认识蜂鸣器、OLED以及湿度传感器。
- 2. 2.用湿度传感器进行创作。


## 所需材料:  
---

- 1 x [BBC Micro:bit](http://www.elecfreaks.com/estore/micro-bit-board.html)
- 1 x USB线
- 1 x [扩展板](http://www.elecfreaks.com/estore/elecfreaks-micro-bit-breakout-board.html)
- 1 x [蜂鸣器](https://www.elecfreaks.com/estore/octopus-passive-buzzer-brick-obpb01.html)
- 1 x [OLED](https://www.elecfreaks.com/estore/iic-oled.html)
- 1 x [湿度传感器](https://www.elecfreaks.com/estore/octopus-soil-moisture-sensor-brick.html)
- 2 x 母对母跳线

**温馨提示: 如果你想要以上所有这些元器件，你可以购买我们的[micro:bit小小发明家套件](https://item.taobao.com/item.htm?spm=a230r.7195193.1997079397.9.z3IMPf&id=564707672256&abbucket=5)。**


## 制作过程  
---

首先，将OLED插入扩展板。
你可以插入3排排针的任意一排。

![](https://i.imgur.com/qOBV7Uf.png)

蜂鸣器连接扩展板上的引脚P0，确保线的颜色和扩展板排针的颜色一致。

![](https://i.imgur.com/ABoiMrD.jpg)

湿度传感器连接扩展板上的引脚P1。

![](https://i.imgur.com/jgTG7i6.jpg)

打开Microsoft MakeCode的编程界面，找到代码抽屉中的Advanced（高级选项）。
点击Advanced（高级选项）来查看更多代码选项。我们需要添加一个代码库来方便我们使用我们的套件。
在代码抽屉底部找到“Add Package”（添加代码库），并点击它。

![](https://i.imgur.com/FOHSrAx.png)

这时会弹出一个对话框。在对话框中搜索“tinker kit”，然后点击下方出现的“tinkercademy-tinker-kit”来下载这个代码库。

![](https://i.imgur.com/G2nV10d.png)

点击代码抽屉中的Tinkercademy类目，找到适合我们套件的积木块。

![](https://i.imgur.com/57H4sCe.png)
![](https://i.imgur.com/DaZC53n.png)

之后，用Tinkercademy类目下方的积木块来初始化OLED。

![](https://i.imgur.com/xAM8RDr.png)

因为此处只有2个条件，所以我们只需要使用1个else-if语句。micro:bit会不断地从湿度传感器上读取数值。 
当湿度小于50，这表明花盆里面的土壤水分不足。因此，蜂鸣器就会响起，OLED屏幕上就会显示“给植物浇水”。
但是当湿度大于50，蜂鸣器就不会响起，OLED屏幕上就会显示“植物状态良好”。

![](https://i.imgur.com/qy2wheV.png)

如果你不想自己亲手编写代码，你可以通过下面的这个链接直接下载程序的所有代码。

[https://makecode.microbit.org/_Ja5AomXm7UVJ](https://makecode.microbit.org/_Ja5AomXm7UVJ)

或者，你也可以通过这个页面下载代码：

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_Ja5AomXm7UVJ" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>


终于完成啦！你已经成功地制作出了一个植物土壤湿度检测装置哦！现在，让我们一起来看看看效果吧！

![](https://i.imgur.com/nD0PGDe.png)

将这些代码下载到micro:bit上。 然后，找到一盆绿色植物，把湿度传感器插入土壤中，看看它的湿度。当土壤水分不足时，蜂鸣器就会响起，告诉你“给你的植物浇水了！”。当土壤水分充足时，OLED屏幕上将显示水分充足，不需要给植物浇水。 

是不是非常有趣呢？


## 常见问题
---


## 相关阅读  
---

[Micro:bit小小发明家课程01:音乐播放器](/Micro_bit_Tinker_Kit_Case_01_Music_Machine_CN/)                         
[Micro:bit小小发明家课程02:智能灯](/Micro_bit_Tinker_Kit_Case_02_Smart_Light_CN/)    
[Micro:bit小小发明家课程03:电子琴](/Micro_bit_Tinker_Kit_Case_03_Electro_Theremin_CN/)    
[Micro:bit小小发明家课程04:报警装置](/Micro_bit_Tinker_Kit_Case_04_Simple_Alarm_Box_CN/)    
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
