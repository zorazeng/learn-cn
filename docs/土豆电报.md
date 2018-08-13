## 土豆电报

不要把土豆留在手里太久，不然你会输掉这个游戏哦！

![](https://i.imgur.com/V5EtA0N.png)

你知道游戏“烫手的土豆”吗？当计时器开始倒计时，你把土豆传给周围的人。倒计时结束后，持有土豆的人就输了。这个游戏特别有趣。

在这个项目中，我们将创建一个类似的游戏，但是作为替代，我们将使用一个虚拟的土豆和micro:bit无线电。

### 发送土豆电报?

除了时钟倒计的时候将土豆传递给周围的人，我们将在micro:bit之间**发送一个数字**。我们可以用`||无线电：无线电||`积木块来实现它。它们使用了micro:bit上的天线，通过射频信号发送数据，正如手机或者是你周围的装置一样。

![](https://i.imgur.com/gWNcq6O.png)

那么，用一个数字来代表一个土豆是什么意思呢？我们需要将时钟**模型化**为与马铃薯一起抛出的**一个数字**。我们这样做是为了用无线电来玩游戏。那么这个土豆时钟有什么特别之处呢？它可以倒计时。当它达到0时，铃声响起。

为了追踪事件，让我们创建一个变量，将它命名为**potato**：

- 如果**potato**的数值为正，玩家就拿到了土豆，并且变量**potato**代表了**剩余时间**。
- 如果**potato**的数值达到0，游戏结束。
- 如果**potato**的数值为负，这就意味着玩家手里并没有土豆。

既然我们知道土豆是什么，我们需要与用户互动。这就是玩家玩游戏的方式：

- 按下按钮`A+B`来启动游戏并发送第一个土豆。
- 当收到一个土豆的时候，屏幕就会显示一些图像。
- 当玩家摇晃micro:bit, 土豆就会被发送至其他玩家的micro:bit。

### 让我们开始编程吧!

#### 初始化

让我们先从创建**potato**变量开始，在 `||基本：当开机时||`将它的值初始化为`-1`。记住，一个负数的值代表你**没有**土豆。我们用`||无线电：无线设置组||`来确保玩家收到了信息。

![](https://i.imgur.com/qZ6FGSk.png)

#### 开始游戏
为了启动游戏，我们响应`A+B`按钮的按下，并给变量**potato**赋一个正数。为了使游戏充满变化，我们用`||数学：选择随机||`积木块来生成一个`10`~`20`之间的数值。

![](https://i.imgur.com/svRoIxj.png)

#### 发送土豆
通过摇晃micro:bit就可以完成发送土豆。如果变量**potato**为正数，我们就拿到了土豆，并且我们可以把它发送出去。在把土豆发送出去后，我们就把变量**potato**设置为`-1`，因为我们没有土豆了。 

![](https://i.imgur.com/E2J9Zze.png)

#### 接收土豆

在积木块`||无线电：在无线接收到数据时运行||`中完成土豆的接收。**receivedNumber**代表了土豆，并且存储在变量**potato**中。

![](https://i.imgur.com/3RGL3VC.png)

#### 倒计时

用一个`||循环：无限循环||`来使时钟倒计时。

- 如果potato等于0 (potato== 0)，你输了！
- 如果potato变量的数值为负数（potato < 0），我们就没有拿到土豆，因此我们可以清空屏幕。
- 如果potato变量的数值为正数(potato > 0)，我们就显示土豆图像，并用这个变量减1。

![](https://i.imgur.com/zqvJZsY.png)

#### 开始玩游戏了!

找到两块或多块micro:bit,将代码下载到micro:bit上。让一个玩家按下按钮A+B来启动游戏，接收第一个土豆。祝你好运！

### 完整代码

![](https://i.imgur.com/5YLmwoE.png)

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_89Vd7tTHs6gf" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>





