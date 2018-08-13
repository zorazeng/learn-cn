## 电报活动

![](https://i.imgur.com/5YwP3z5.png)

在两块micro:bit之间发送电报，和你的朋友们进行通信吧！
时长：~30分钟

## 活动

### 制作

让我们在两块micro:bit之间发送电报吧！

![](https://i.imgur.com/dn4MGLJ.png)

### 材料

- 2块micro:bit、一个电池盒和2节7号电池
- 4个鳄鱼夹

## 步骤

#### 步骤 1

![](https://i.imgur.com/Zlegdj4.png)

将**第一个**鳄鱼夹连接到micro:bit上的**GND**引脚。

#### 步骤 2

![](https://i.imgur.com/skaTcpC.png)

将**第二个**鳄鱼夹连接到micro:bit上的**3V**引脚。

#### 步骤 3

![](https://i.imgur.com/PoNBZdS.png)

将**第三个**鳄鱼夹连接到micro:bit上的**P1**引脚。

#### 步骤 4

![](https://i.imgur.com/q6BQFR4.png)

将**第四个**鳄鱼夹连接到micro:bit上的**P2**引脚。

#### 步骤 5

![](https://i.imgur.com/vwNZeQo.png)

将**第一个**鳄鱼夹连接到第二块micro:bit上的**GND**引脚。

#### 步骤 6

![](https://i.imgur.com/qNnbyLH.png)

将**第二个**鳄鱼夹连接到第二块micro:bit上的**3V**引脚。

#### 步骤 7

![](https://i.imgur.com/5MSU6ef.png)

将**第三个**鳄鱼夹连接到第二块micro:bit上的**P2**引脚。

#### 步骤 8

![](https://i.imgur.com/AqTusdQ.png)

将**第四个**鳄鱼夹连接到第二块micro:bit上的**P1**引脚。

#### 步骤 9

![](https://i.imgur.com/M8M7SU3.png)

## 代码

让我们创建代码：当用户按下micro:bit上的按钮**A**，micro:bit将会通过鳄鱼夹线发送一段脉冲到负责接收的micro:bit上，并点亮它上面的一颗LED灯。

确保发送和接收的线“平行地”在两块micro:bit之间运行，也就是：一块micro:bit上的**P1**连接到了另一块micro:bit上的**P2**，并且反之亦然。正如在制作部分的图片所显示的那样。这样我们就能在两块micro:bit上运行相同的代码。 

### 步骤 1

我们先从一个积木块开始--数字读取**高**电压（一个数字`1`）到`P1`，也就是将这个值发送到micro:bit上的引脚P1。这个积木块可以在工具栏高级选项中的**引脚**抽屉中找到。

![](https://i.imgur.com/ZBxSOfk.png)

### 步骤 2

为了显示我们正在发送`1`，我们添加了一个积木块`绘图 x y`，点亮了LED屏幕(2，2)中间的一颗LED灯：

![](https://i.imgur.com/4cdiLGq.png)

### 步骤 3

既然我们知道如何发送信号，我们只想要在按钮**A**被按下的时候发送它。从逻辑抽屉中选择一个`如果 则 否则`积木块（现在你将在`否则` 部分留白)。添加一个检查，检测按钮**A**什么时候被按下。从**输入**抽屉中选择一个`当按钮被按下`积木块，并将这个积木块移动到`如果 则 否则`积木块中的`则`部分。

![](https://i.imgur.com/h0OdEUw.png)

### 步骤 4

对于`否则`部分（当按钮**A**没有被按下），我们想执行在`则`部分相反的动作，也就是将引脚`P1`的数值变**低** （数字0），并在负责发送的那块micro:bit上绘制相应的LED灯： 

![](https://i.imgur.com/DvVcvAm.png)

### 步骤 5

让我们将这些代码都放入到一个`无限循环`积木块中，这样后台运行的代码会一直检查按钮**A**，并发送相应的信号给负责接收的micro:bit。修改你的代码，添加下面的积木块。将代码下载到其中一块micro:bit，按下并弹起按钮**A**几分钟。

![](https://i.imgur.com/p1PyuMo.png)

发送部分已经完成了，所以现在我们将添加接收部分的代码。

### 步骤 6

负责接收的micro:bit需要数字读取它的某个引脚。这个引脚通过鳄鱼夹线接收另一块micro:bit发送给它的**P2**引脚的值。让我们先去到**引脚**抽屉，添加一个`数字读取引脚`并将引脚的数值改为`P2`。

现在，我们想检查从`P2`读取的数值，并检查它是否是**高**（1）或**低**（0）。去到**逻辑**抽屉，选择一个`如果 则 否则`积木块，然后返回**逻辑**抽屉，选择较运算符`0 = 0`。 插入一个`数字读取引脚`积木块，将它作为一个运算数，并把数值1作为另一个运算数。

我们将点亮屏幕右下角（4，4）的LED灯，显示我们已经收到了一个**高**值。如果没有收到，则把它熄灭。

确保你的代码看起来像这样：

![](https://i.imgur.com/FQ66MJ6.png)

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_3g4Rsf6zvgPE" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>

你的电报已经完成了！

### 步骤 7

那么，让我们试一试吧！

1. 用USB将第一块micro:bit连接到电脑，将电报代码下载到其中。
2. 断开第一块micro:bit的连接。
3. 用USB将第二块micro:bit连接到电脑，将电报代码下载到其中。
4. 断开第二块micro:bit的连接。
5. 将电池组连接到其中一块micro:bit上。
6. 玩家可以轮流按下他们的micro:bit上的按钮A来玩这个电报游戏。







