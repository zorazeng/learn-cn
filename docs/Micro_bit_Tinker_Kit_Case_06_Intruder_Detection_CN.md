
## Intruder Detection  


在这个项目中，我们将创造一个入侵检测系统。当有人开门的时候，它就会发出警报，而房屋的状态也会显示在OLED屏幕上。

## 所需材料：  
---

- 1 x [BBC micro:bit](http://www.elecfreaks.com/estore/micro-bit-board.html)
- 1 x USB线
- 1 x [扩展板](http://www.elecfreaks.com/estore/elecfreaks-micro-bit-breakout-board.html)
- 1 x [碰撞传感器](https://www.elecfreaks.com/estore/octopus-crash-sensor-brick.html)
- 1 x [OLED](https://www.elecfreaks.com/estore/iic-oled.html)
- 1 x [蜂鸣器](https://www.elecfreaks.com/estore/octopus-passive-buzzer-brick-obpb01.html)
- 2 x 母对母的跳线

**温馨提示: 如果你想要以上所有这些元器件，你可以购买我们的[micro:bit小小发明家套件](https://item.taobao.com/item.htm?spm=a230r.7195193.1997079397.9.z3IMPf&id=564707672256&abbucket=5)。**


## 目标：  
---

- 了解碰撞传感器、OLED和蜂鸣器。
- 用OLED进行创作。
- 用碰撞传感器进行创作。


## 制作过程  
---

### 步骤 1 – 元器件连接  

将micro:bit插入扩展板，并用USB线连接micro:bit。

![](https://i.imgur.com/cvJnbqE.jpg)

然后，用跳线将蜂鸣器连接到扩展板上的引脚P0。如下图所示，插入OLED。你可以将它插入到扩展板上3排排针孔的任意一排。

![](https://i.imgur.com/3benydL.jpg)

将碰撞传感器连接到扩展板上的引脚P1。确保线的颜色和扩展板上引脚的颜色一致。

![](https://i.imgur.com/YvQkd81.jpg)


### 步骤 2 – 编程前的准备  

![](https://i.imgur.com/qPgEmnW.jpg)

我们将添加一个代码库来方便使用我们套件中的元器件。在代码抽屉中点击Advanced，查看更多代码选项，并在代码抽屉底部找到Add Package。

![](https://i.imgur.com/IWhPZeP.png)

这将会弹出一个对话框。在对话框中搜索“tinker kit”， 然后点击下载这个代码库。

![](https://i.imgur.com/b0vriWO.png)

注意：如果你收到提示说一些代码库因为不兼容的问题将被删除，你可以选择根据提示操作，或者在项目文件的菜单中选择新建一个新项目。


### 步骤 3 – 编程  

![](https://i.imgur.com/OKjXb0c.jpg)

点击代码抽屉中的Tinkercademy, 找到与我们元器件相应的积木块。

![](https://i.imgur.com/UwHfSVv.jpg)

你应该在开始的时候初始化OLED。64和128分别代表了OLED的高度和宽度。

![](https://i.imgur.com/GIhLCLU.jpg)

因为这里只有两个条件，所以我们只需要一个“else-if”语句。
当碰撞传感器被触发，蜂鸣器响起，OLED屏幕上将会显示“Intruder Detected”（检测到入侵）。否则，蜂鸣器不会响起，OLED屏幕上显示“The house is safe”（房屋处于安全状态）。

如果你不想自己亲手编写代码，你可以从下面这个链接直接下载程序的完整代码：

[https://makecode.microbit.org/_A0zFxqMPMXbo](https://makecode.microbit.org/_A0zFxqMPMXbo)

或者，你也可以从下面这个页面下载：

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_A0zFxqMPMXbo" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>


### 步骤 4 – 成功!  

太棒啦！你已经创造出了一个入侵检测器哦！


## 常见问题
---


## 相关阅读  
---

[Micro:bit小小发明家课程01:音乐播放器](/Micro_bit_Tinker_Kit_Case_01_Music_Machine_CN/)                     
[Micro:bit小小发明家课程02:智能灯](/Micro_bit_Tinker_Kit_Case_02_Smart_Light_CN/)    
[Micro:bit小小发明家课程03:电子琴](/Micro_bit_Tinker_Kit_Case_03_Electro_Theremin_CN/)  
[Micro:bit小小发明家课程04:报警装置](/Micro_bit_Tinker_Kit_Case_04_Simple_Alarm_Box_CN/)  
[Micro:bit小小发明家课程05:土壤湿度检测](/Micro_bit_Tinker_Kit_Case_05_Plant_Monitoring_Device_CN/)  
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
