## Salute!（micro:bit小组数学游戏）

Salute!是一个简单的数学游戏。玩家从一叠卡片中随机选择一张数字卡，在不看卡片的情况下，直接把卡片贴在他们的额头上正如在“Salute”（敬礼）这个游戏中一样。另一个玩家决定是否将两张卡片的数字相加或者进行数学运算，然后宣布计算结果。根据对方玩家持有的卡片和听到的数字结果，每个玩家尝试着找出他们所持有的卡片。

### 活动目的

- 这个小组游戏适合于课堂活动或者朋友聚会。
- 将每个必要的步骤分解，进行编程，然后玩这个游戏。这个数学游戏将会使用micro:bits。
- 创建一个程序，在micro:bit的LED点阵上显示一个随机数（在合适的范围内），并将这个程序成功地下载到micro:bit上。
- 你也可以创建一个程序来记录micro:bit游戏的得分，并将这个程序成功地下载到micro:bit上。或者，在游戏过程中，用一个头箍来固定住前额的micro:bit和电池。
- 玩这个micro:bit游戏。这个游戏分3个人一组来玩。

根据参考链接提供的信息，尽快熟悉游戏的玩法吧！

### 所需材料

- 2~3块micro:bit，带电池组和USB线。
- 笔和纸
- 用于制作头箍来固定住micro:bit的材料。（可选）

### 游戏编程

#### 2个玩家

- 给2块micro:bit编程，让其显示一个特定范围内的随机数，这是基于一个“Salute”（敬礼）。一个“salute”（敬礼）是一次达成共识的事件/输入，学生没有看他们的LED点阵而达成的共识。
- 包括一个循环，用于检验数字是否大于0或1，以及这些数字是否将会包括在这个游戏中。
- 如果这个范围的上限值大于9，用一个循环来多次显示这个数字或者提供另一种方式重新显示数字。

#### 3个玩家

如果使用了3块micro:bit, 则给第三块micro:bit编程，用它的按钮A和B来记录游戏的得分，并根据一个不同的事件(例如：同时按下按钮A和B) 来显示得分。这里应该还有一种方式来重置得分以进行下一场游戏。

### 制作数字卡片

选择一个0~9之间的随机数。

![](https://i.imgur.com/LywvFi5.png)

选择一个1~9之间的随机数。

![](https://i.imgur.com/jFIxpKI.png)

### 记录得分

当按钮A或B被按下的时候，得分记录程序就会给玩家加1分。按下`A+B`，则显示当前的赢家和得分。通过翻转micro:bit来重置得分。 

![](https://i.imgur.com/pXaz6H6.png)

### 玩游戏

在游戏开始之前，要想清楚游戏将会有多少回合或者游戏每个回合会持续多久。并且，还要思考如何判定一个平局：两个玩家都能够加1分，还是两个玩家都不能够加1分？

- 玩家1和2将会把micro:bit戴在前额，面对面地站着或者坐着，这样他们就能够看到另一个玩家的micro:bit的LED屏幕。玩家应该不能够看到他们自己的micro:bit的LED屏幕。注意：创建一个小组，让组员们将micro:bit戴在前额，并创造出一个动作，让组员们通过摇头来选择一个数字，这是非常有趣的。
- 3号玩家将会坐着或者站着，这样他们就能够看到玩家1和玩家2的micro:bit。
- 玩家3将会说“Salute!”（敬礼），并且玩家1和玩家2应该用他们的micro:bit相互“salute”（敬礼), 这时他们的micro:bit屏幕上会显示一个随机数。
- 玩家3迅速地将玩家1和玩家2的micro:bit屏幕上显示的这些数字相加（如果是在做加法或者减法的游戏的话）或者相乘（如果是做乘法或者除法的话）。然后，玩家3应该会说出结果。如果想要强调数学词汇的话，需要玩家3使用合适的数学词汇: “...之和等于...。” 或者“...的结果是..。”
- 然后，玩家1和玩家2试着以最快的速度计算并说出他们的micro:bit上显示的数字。谁先说出micro:bit上显示的数字，谁就赢得了该回合的游戏。 如果在一次乘法的游戏中使用了0，看到对方micro:bit上显示0的玩家说“任意一个数字”都可以作为正确的答案。如果你想强调正确地使用数学词汇的话，玩家就必须说整个数学的公式而并不仅仅只是说数字。例如：如果在一次乘法公式的游戏中，玩家1的micro:bit显示了一个2，玩家2的micro:bit显示了一个6，那么玩家1或者玩家2之间谁正确地说出了“2乘以6 (或者6乘以2)等于12”，谁就会赢得该回合的游戏。 
- 之后，玩家3统计得分情况：如果第三块micro:bit经过编程可以用来记录得分，那么当玩家1赢得了一个游戏回合，玩家3就按下按钮A；如果玩家2赢得了一个游戏回合，那么玩家3就按下按钮B。如果这个游戏中只是用了2块micro:bit, 那么玩家3应该在纸上记录得分情况。
- 在所以游戏回合的末尾（或者指定的时间节点），玩家双方的总体得分情况都应该被记录在纸上。如果第3块micro:bit经过编程可以用来统计得分，那么玩家3应该将得分情况显示在micro:bit上，并将他们的得分写在一张计分表上。这张计分表通常都会写有玩家的姓名，而不是玩家的编号，因为玩家可以互换位置。

如果时间允许的话，玩家们应该互换位置（例如：玩家1变成玩家2，玩家2变成玩家3，以及玩家3变成玩家1）并重复相同游戏时长或者游戏回合，直到每个人都有一次成为玩家3的机会。如果时间不允许的话，下次玩游戏的时候再互换位置。

### 变化

- 如果人数足够，可以组成4人一组的小组，那么玩家3将会说“Salute!”（敬礼！）并将两张卡片上的数字相加或者计算它们的结果，正如之前一样。玩家4可以是记录得分的人，并且充当任何平局的裁判，又或者玩家4有另外一块显示了数字的micro:bit，玩家们需要用这3块micro:bit上显示的数字来进行计算。

- 老玩家把这个游戏介绍给新玩家的时候，要确保使用一个合适的数字范围作为得分等级。老玩家，或者新老玩家一起，可以制作一些类似头箍类的东西来将micro:bit固定在前额上。然后，老玩家再告诉新玩家游戏该怎么玩。

- 如果只使用了2块micro:bit并想要记录得分的话， 将记录得分的代码添加到其中一块micro:bit上，并使用那块micro:bit上的AB按钮来记录得分。


## 参考

[Salute：一个能提高数学运算能力的游戏](https://www.brighthubeducation.com/lesson-plans-grades-3-5/28715-play-the-game-salute-to-reinforce-math-facts/): 这是原来用卡片来玩这个游戏的一个例子。 

此外，你还可以通过这个视频来了解这个游戏是怎么玩的：

[https://www.youtube.com/watch?v=DJBMbSUGZsc](https://www.youtube.com/watch?v=DJBMbSUGZsc) How to Play Salute!

这个数学游戏的项目是由[Vicky Sedgwick](https://about.me/vicky.sedgwick)制作的。它是基于[Todd Lash](https://twitter.com/Todd_Lash)创作的最初的游戏理念。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_Ph44k5Dx9YMX" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>