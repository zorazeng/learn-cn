## 计时门槛

这个项目用家用材料解释了计时门槛的工作原理。

### 计时门槛

连接到micro:bit上的两个门槛可以检测经过它们的小车。

![](https://i.imgur.com/jJGrpgE.png)

当小车经过门槛`0`，它通过`当引脚被按下`积木块向micro:bit发出了一个事件。micro:bit将时间记录在变量`t0`中。

![](https://i.imgur.com/HhNoFNt.png)

当当小车经过门槛`1`，它通过`当引脚被按下`积木块向micro:bit发出了一个事件。micro:bit将时间记录在变量 `t1`中。

![](https://i.imgur.com/BhWGIFe.png)

接下来是一些数学和物理。小车经过两个门槛的时间是根据t1-t0之间的差来计算出。用两个门槛之间的距离除以时间，我们就得到了小车的速度哦！

![](https://i.imgur.com/Zzytibg.png)

### 材料

- 硬纸板
- 铝箔
- 双面胶（地毯胶布）
- 4个鳄鱼夹
- 1块micro:bit
- 1根USB线

![](https://i.imgur.com/DFME2yL.png)

### 积木块

![](https://i.imgur.com/OYLnquP.png)

### 制作门槛

将两条铝箔展开，平铺在硬纸板上。这将会是我们的传感器。
在硬纸板上粘上两条双面胶，把双面胶的保护膜撕开。

![](https://i.imgur.com/sG70tSs.png)

将铝箔放在双面胶上，用手压紧，使铝箔牢牢地粘在硬纸板上。

![](https://i.imgur.com/N76i10K.png)

将四周和中间没有粘在双面胶上的铝箔撕掉，清除多余的铝箔。在两条铝箔之间留出足够的空隙，让它们不会挨在一起。

![](https://i.imgur.com/H2wQS3u.png)

在每条铝箔上夹上一个鳄鱼夹。

![](https://i.imgur.com/WvqfZeX.png)

将鳄鱼夹分别连接到micro:bit上的`GND`和`P0`引脚。

![](https://i.imgur.com/64xTmMW.png)

现在门槛已经可以使用了！你的电路应该看如下图所示：

![](https://i.imgur.com/tD1kurd.png)

### 用代码检测小车

micro:bit提供了一个事件`当引脚被按下`。当检测到`GND`和一个引脚之间的电路，这个事件就形成了。电路的导体可能是一根线，甚至是你的身体。我们将把一片铝箔贴在小车底部。当小车经过门槛的时候，它连接了两条铝箔，闭合电路，并触发事件。 

打开[代码编辑器](https://makecode.microbit.org/)，创建一个新项目，并添加下面的积木块。注意：这里我们使用的引脚是`P0`。

![](https://i.imgur.com/Eti7lzX.png)

用我们的手指来测试代码。我们看到当手指压在两条铝箔上的时候，micro:bit上的一列LED灯被点亮了。

[https://youtu.be/zi_-NAmdDpY](https://youtu.be/zi_-NAmdDpY)

### 升级小车

在这节课程中，我们随机选择了一辆玩具车，并将铝箔粘贴到了小车底部。当小车经过门槛的时候，它将会连接门槛的两边，并触发事件。确保添加足够多的铝箔来获得好的连接。

![](https://i.imgur.com/2LySkGH.png)

移动小车（缓慢地）经过门槛，你将会看到它触发了`当引脚被按下`事件。

[https://youtu.be/M3DIUvDPlIA](https://youtu.be/M3DIUvDPlIA)

它不会一直有效。为什么呢？有时候，长时间的分离使铝箔无法连接这两条铝箔。这是因为我们传感器的质量较差。为了解决这个问题，你将需要使用一个更好的传感器，或者一个红外探测器，又或者一个霍尔效应传感器。

### 添加第二道门槛

用铝箔和双面胶重复同样的步骤来创建第一个门槛。

![](https://i.imgur.com/EczuaoT.png)

将鳄鱼夹夹在micro:bit上的`GND`和`P1`引脚。

![](https://i.imgur.com/NW9TCAP.png)

### 检测第二道门槛

因为第二道门槛连接到了引脚`P1`，我们添加了第二个`当引脚被按下`事件来显示2列LED灯。

![](https://i.imgur.com/XpKXhDc.png)

小车滚过这两道门槛，你可以看到事件在小车经过第一道门槛的时候被触发，接着轮到第二道门槛。

[https://youtu.be/N4bWQcu6yWs](https://youtu.be/N4bWQcu6yWs)

### 计算

micro:bit有一个可以准确计时的时钟。它可以测量micro:bit已经开启了多少秒。我们将记录每道门槛在变量`t0`和`t1`的时间。我们用`t1` 和`t0`来计算两道门槛之间的时间差。

![](https://i.imgur.com/RCUzRMM.png)

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_AYTi7sMt8XCq" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>

[https://youtu.be/piyym_ux1EM](https://youtu.be/piyym_ux1EM)

### Computing velocity

计算门槛之间的距离，应用牛顿定律来计算小车的速度（小车跑的有多快）。

> v = d / t

我们将让你自己尝试给这个项目编程哦！



















