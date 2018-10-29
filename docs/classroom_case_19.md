## 情绪无线电

![](https://i.imgur.com/wkP2X5J.png)

这个项目用无线电将你的心情分享到别的micro:bit上。当你按下按钮`A`，你的朋友们将会看到一个**笑脸**。 当你按下按钮`B`，他们将会看到一个哭脸。

### 发送笑脸

虽然micro:bit不能理解情绪，但是它却擅长理解数字。事实上，用无线电可以在micro:bit之间发送数字，正如一部手机可以发送文本信息一样。

让我们添加一些积木块，当按钮`A`被按下的时候，发送一个数字。假设`0`是发送笑脸的“情绪代码”。

![](https://i.imgur.com/RyfOTCW.png)

### 接收笑脸

添加一个`||无线电：当无线电接收到||`积木块，当收到一则新的“情绪”信息时，则运行代码。变量`receivedNumber`包含了已发送的数值。因为我们决定用`0`代表**笑脸**，我们添加一个条件语句`||逻辑：如果 则||`来显示这个图标。

![](https://i.imgur.com/JB8lvwh.png)

### 发送哭脸

以同样的方式添加其他的情绪到我们信息APP上。我们决定用`1`作为代表**哭脸**的“情绪代码”。我们可以添加一个按钮`B`的事件来发送那个代码。

![](https://i.imgur.com/mrrIepP.png)

在`||无线电：当无线电被接收||`积木块中，我们添加了另一个条件语句`||逻辑：如果 则||`来处理**哭脸**的“情绪代码”。

![](https://i.imgur.com/wvXYpwD.png)

这就是我们要编写的所有代码了！将你的代码下载到多个micro:bit上，试一试吧！

### 挑战

试着添加一个新代码，并使用`||输入：当震动||`事件来发送它。

### 完整代码

![](https://i.imgur.com/CqKxsoK.png)

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_LwsbHvdu1XPA" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>



