## 赛车

改装一辆赛车，用你的micro:bit和Kitronik元件来控制它吧！

[https://youtu.be/xQJCZwVvjyw](https://youtu.be/xQJCZwVvjyw)

##### 注意

这个活动涉及到打开一个电子玩具，切断它的接线，并重新连接它的线。你的玩具有可能完全报废。改造的风险和回报是并存的！ 

### 材料

- 带4节或6节5号电池的玩具赛车
- 1块micro:bit（如果你想用无线电控制，可以选用两块micro:bit)
- 剪线钳
- 小十字螺丝刀
- 1个Kitronik电机驱动器


### 我们的改造计划是怎样的？

大部分玩具赛车的运转都采用了3个小电机：

- 1个直流电机驱动后轮 
- 1个直流电机驱动前轮 
- 1个直流电机将前轮转向

我们现在要做的事打开小车，去除里面的电子控制器，将它替换成Kitronik的可以驱动2个直流电机的电机驱动器。我们将这两个电机的力臂连接到一个控制器上，转动电机到另一个控制器上。

连接电机驱动器之后，我们将使用一块micro:bit来控制它。此外，我们可以用另一块micro:bit作为一个无线电控制器，来控制小车里的micro:bit。

##### 如何获取用于改造的小车

问一下你的朋友或者家人，看看他们有没有闲置的旧赛车。去杂货店以及其他二手店逛逛，看看有没有捐赠的玩具赛车。


## 活动
## 制作

将micro:bit改装到小车上吧！

[https://youtu.be/gH__3l_oDeM](https://youtu.be/gH__3l_oDeM)

### 步骤 1：移除电池

确保小车上所有的电池都被移除。

### 步骤 2：移除车身和电子盖

移除用于保护电子控制器的车身和塑料件，这样你就可以改造它。将你移除的所有螺丝放好，待会儿你还会用到它们哦！

### 步骤 3：断开原来电路的连接

根据电机和电线来找到控制器。将电线尽可能地剪短到电路板的表面（神经外科）。最后你将保留8条线：**2**条用于供电，**2**条用于使电机转向，以及**4**条线用于连接电机力臂。

你可以将旧的控制器取出以腾出更多的空间。

![](https://i.imgur.com/igK4qqW.png)

### 步骤 4：准备线

用剪线钳去除每根电线上大约1/4英寸（1/2 cm）的绝缘体，使金属导体露出，这样你就能将它连接到舵机上。

![](https://i.imgur.com/BR38O3Q.png)

### 步骤 5：连接电池 

- 将电池连接到电机驱动器的电源输入口。确保**+**（正极）线连接到**+**（正极）接口！
- 将两个电机的扭矩连接到电机驱动器上的**电机1**接口。确保当你连接的时候，线的颜色和接口的颜色一致，这样你的车轮才会转动到正确的方向哦！
- 将剩余的电机线连接到**电机2**接口。

![](https://i.imgur.com/Qc30shb.png)

### 步骤 6：插入micro:bit 

这大概是最简单的一步。将micro:bit插入边缘接口直到卡紧在凹槽中。

### 步骤 7：在车盖上切出一个小孔来放置micro:bit(可选）

在原来控制器的保护盖上，位于边缘接口上方的部分，切出一个小孔。这样既可以保护Kitronik的控制器，又能将你的micro:bit完美地插入到边缘接口的凹槽中。

![](https://i.imgur.com/oJcEw8s.png)

### 步骤 8: 装上车身（可选）

根据车的大小和形状，你也许可以将车身装回到车子顶部。如果不行的话，用一些硬纸板、剪刀和一把胶枪来制作一个新的车身。

### 步骤 9：喷漆（可选）

当你装好了车身后，给它添加一些造型吧！

![](https://i.imgur.com/LnvavWU.png)

这就是我们的赛车了。开始编程吧！

## Code

### 步骤 1：添加Kitronik代码库

Kitronik有一个代码库，里面有给电机驱动器编程的积木块。我们需要将它添加到我们的代码中。

- 点击**高级选项**
- 点击**添加代码库**
- 输入`kitronik`，按下**Enter**键
- 选择**kitronik-motor-driver**代码库

在这个代码库加载完成后，你应该能在工具栏中看到一个新的**Kitronik**类目。

### 步骤 2：转圈圈 

[https://youtu.be/pD6tM1nXCPA](https://youtu.be/pD6tM1nXCPA)

在第一个程序中，当用户按下按钮A，小车就会原地转圈5秒。通过让两个电机控制器转动5秒就可以实现它。

![](https://i.imgur.com/AYoCs3u.png)

##### 保护你的电子元件

当你将micro:bit连接到电脑的时候，确保你已经将它从边缘接口处拔出。这将会保护micro:bit，避免潜在的电子问题。
根据你的电线连接到电机驱动器上的方式，你的车可能向后移动，而不是向前移动。如果是这样的话，你可以切换接线，或者改变代码中的`MotorDirection`，让小车朝正确的方向行驶。

### 步骤 3：数字8

[https://youtu.be/agor9wtiAkE](https://youtu.be/agor9wtiAkE)

与5秒后停车相反，我们将转向电机转到另一个方向。这将会产生一个8字形的路径。

![](https://i.imgur.com/WzsCxSu.png)

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_VAza2eCKgDE6" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>

太棒了！驱动小车的代码已经编写完成了！现在找到另一块micro:bit，用它来遥控小车。

## 连接

### 步骤 4：遥控

[https://youtu.be/XXesoUC0XBU](https://youtu.be/XXesoUC0XBU)

我们可以用micro:bit上的无线电来遥控这个玩具车。第二块micro:bit将会发出指令来控制刹车和转向。

![](https://i.imgur.com/rJ5qv7M.png)

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_VzeUAY1X4AAV" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>





