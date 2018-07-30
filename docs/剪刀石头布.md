## 剪刀石头布

用micro:bit制作剪刀石头布游戏，并挑战你的朋友们。

![](https://i.imgur.com/9MHnzYj.png)

持续时间: ~20分钟。

### 材料

- micro:bit、电池盒和2节7号电池
- 1卷胶带 (如果你想要另一种颜色，则可能需要2卷）
- 尼龙搭扣

### 活动

#### 设置

##### 步骤 1 - 胶带剪切

剪下2段大概9-10英寸长的胶带，将带有粘性的一面粘在一起，使其成为一段胶带（这有点难做！）。这个就是你的腕带。

![](https://i.imgur.com/NwUoy2N.png)

##### 步骤 2 - 将micro:bit和电池组粘上

将腕带绕成一个圆环，并将micro:bit粘贴在环形腕带的中央。

![](https://i.imgur.com/Fvg8pL7.png)

将电池组连接到micro:bit上，并把它粘在micro:bit背面的腕带上。

##### 步骤 3 - 添加尼龙搭扣

将尼龙搭扣安装在腕带两端，作为紧固装置。你可能需要根据你的手腕来调节腕带的大小。

![](https://i.imgur.com/Ggn8v4M.png)

##### 步骤 4 - 装饰它吧!

用贴纸、闪钻、标签之类的东西来装饰你的腕带。

![](https://i.imgur.com/NmTjyry.png)

#### 代码

##### 步骤 1

当摇晃micro:bit的时候，我们想让micro:bit选择剪刀、石头或者布。选择一个`当摇晃`积木块，当你摇晃micro:bit的时候，它就会运行一部分程序。 

![](https://i.imgur.com/SgomVw5.png)

##### 步骤 2

添加一个`tool`变量来存储用`选择随机`计算出的随机数。
当你摇晃micro:bit的时候，它会选择一个从`0`到`2`的随机数，并将它存储在变量`tool`中。(这个变量被称为`tool`是因为剪刀、石头和布是你用来挑战朋友们的工具！）

![](https://i.imgur.com/q9VGk2e.png)

在后面的一个步骤中，每个可能的数字（0、1或2）对应了它们各自的图片。当它对应的数字被选中的时候，它的图片会显示在micro:bit屏幕上。

##### 步骤 3

在`选择随机`的下方放置一个`if`积木块，并检查`tool`是否等于`0`。

![](https://i.imgur.com/8ZJIt6y.png)

##### 步骤 4

在`if`积木块中，放置一个`显示LED`积木块来显示一块布的图片。

![](https://i.imgur.com/cv3jOGX.png)

##### 步骤 5

在`if`积木块的下方添加一个`else if`积木块，并检查`tool`是否等于`1`。
Click on the gearwheel icon to open up the `if` editor; then drag and drop an `else if` block in the `if` editor.

![](https://i.imgur.com/jqSPChm.png)

##### 步骤 6

Place a `show leds` block under the else if and draw a rock image on the screen.

![](https://i.imgur.com/voWKf9t.png)

##### 步骤 7

将一个带有剪刀图片的`显示LED`积木块添加到`否则`部分的下方。
你不需要检查`tool`是否等于`2`，因为`2`是`0`, `1`,和`2`中剩下的唯一一个数字。这就是为什么你可以使用一个`否则`而不是一个`否则如果为`的原因。

![](https://i.imgur.com/ZgWLqn2.png)

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_fFfPbhbwWimT" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>



