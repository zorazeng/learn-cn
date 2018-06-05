

## Step 0: Pre-build Overview    

![](https://i.imgur.com/mNlJj4l.png)  


## 步骤 0: 项目简介  
---  

![](https://i.imgur.com/mNlJj4l.png)

在这个项目中，我们将会制作一个简易的报警装置来提醒屋主有人偷东西。当碰撞传感器检测到物体被拿走，红色的LED将会闪烁。如果没有检测到物体被拿走，绿色的LED将会一直亮着。我们可以在 OLED 屏幕上看到这个装置的状态。


## 所需材料:  
---  

- 1 x [BBC micro:bit](http://www.elecfreaks.com/estore/micro-bit-board.html)
- 1 x USB线
- 1 x [扩展板](http://www.elecfreaks.com/estore/elecfreaks-micro-bit-breakout-board.html)
- 1 x [LED模块](https://www.elecfreaks.com/estore/octopus-5mm-led-brick-obled-white.html)
- 1 x [碰撞传感器](https://www.elecfreaks.com/estore/octopus-crash-sensor-brick.html) 
- 1 x [OLED](https://www.elecfreaks.com/estore/iic-oled.html)
- 1 x LED
- 2 x 母对母跳线

**温馨提示: 如果你想要以上所有这些元器件，你可以购买我们的[micro:bit小小发明家套件](https://item.taobao.com/item.htm?spm=a230r.7195193.1997079397.9.z3IMPf&id=564707672256&abbucket=5)。**


## 目标:  
---

- 认识LED模块、普通的LED灯、碰撞传感器以及OLED模块。 
- 用不同类型的LED来进行创作。
- 用碰撞传感器和OLED来进行创作。


## 制作过程  
---

### 步骤 1 – 元器件连接  

![](https://i.imgur.com/208tSHD.jpg)

把LED模块连接到P1。

![](https://i.imgur.com/wGQpzcn.jpg)
![](https://i.imgur.com/9yVjSuC.jpg)

如上图所示，用USB线连接micro:bit，再把micro:bit插入到扩展板上。然后，将碰撞传感器连接扩展板上的P0，LED模块连接P8。确保线的颜色和扩展板上的颜色一致。
最后，将OLED模块插入扩展板上3排排针的任意一排插孔。

![](https://i.imgur.com/LQkLriL.jpg)

### 步骤 2 – 编程前的准备  
我们需要添加代码库来方便我们使用准备好的元器件。点击代码抽屉中的Advanced，查看更多的代码选项，并在下拉菜单底部点击Add Package。

![](https://i.imgur.com/W9LqWIQ.jpg)

此时，将弹出一个对话框。在对话框中搜索“tinker kit”， 然后点击下载这个代码库。

![](https://i.imgur.com/JjXJhoP.png)

注意：如果你收到提示说一些代码库因为不兼容的问题将被删除，你可以选择根据提示操作，或者在项目文件的菜单中选择新建一个新项目。


### 步骤 3 – 编程  

![](https://i.imgur.com/yVtxeb2.jpg)

接下来，使用Tinkercademy项下的积木块来初始化OLED和碰撞传感器。如上图所示。

![](https://i.imgur.com/z6Gzehg.jpg)

这个部分的代码可以使红色的LED灯持续闪烁。你可以通过改变暂停的间隔时间来调整LED灯闪烁的速度。

![](https://i.imgur.com/6avB2r8.jpg)

因为这里只有2个条件，所以我们只需要一个“else-if”语句。当碰撞传感器上被按下，绿色的LED将被点亮。否则，红色的LED灯将会持续闪烁。


如果你不想自己动手编写这些代码的话，你可以从下面这个链接下载程序的完整代码：

[https://makecode.microbit.org/_LvC6e0UfWH7c](https://makecode.microbit.org/_LvC6e0UfWH7c)

或者，你也可以从下面这个页面下载代码：

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_LvC6e0UfWH7c" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>


### 步骤 4 – 成功!  

接下来，让我们一起把代码下载到micro:bit，让代码运行吧！然后，再找本书或者其他什么东西放到装置的顶部，看一看下面会发生什么。我们可以看到绿灯被点亮，正如图中所示。然后，把书或者你放置的其他东西拿走，绿灯熄灭，红灯开始不停地闪烁。

![](https://i.imgur.com/wpyHSOF.jpg)


## 常见问题
---


## 相关阅读  
---

[Micro:bit小小发明家课程01:音乐播放器](/Micro_bit_Tinker_Kit_Case_01_Music_Machine_CN/)                         
[Micro:bit小小发明家课程02:智能灯](/Micro_bit_Tinker_Kit_Case_02_Smart_Light_CN/)  
[Micro:bit小小发明家课程03:电子琴](/Micro_bit_Tinker_Kit_Case_03_Electro_Theremin_CN/)    
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
