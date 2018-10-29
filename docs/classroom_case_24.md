## 萤火虫

将你的micro:bit变成萤火虫。

[https://youtu.be/ZGvtnE1Wy6U](https://youtu.be/ZGvtnE1Wy6U)

### 萤火虫如何同步？

去到 [http://ncase.me/fireflies/](http://ncase.me/fireflies/)，阅读有关萤火虫同步现象的信息。

### 萤火虫编程

我们想用多块micro:bit（每块micro:bit充当一个萤火虫）创建虚拟萤火虫。让我们回顾一下文章中的一些要点：

#### “每只萤火虫都有自己独立的内部时钟......”

在这个案例中，时钟就像一个计数器，因此我们将在程序中先添加一个clock变量。

![](https://i.imgur.com/bVHj1db.png)


#### “......每当时钟'敲响十二'时，它就会闪烁。”

我们可以用一个`无限循环`来重复运行代码，增加时钟时数。当时钟到达“中午”（让我们选择8为正午）时，我们会用游戏得分的动画短暂开启屏幕。

![](https://i.imgur.com/M5BX0Mt.png)


#### 当你看到附近的萤火虫闪烁时，稍微向前推动你的时钟

micro:bit可以发送无线电信息到相邻的一块micro:bit上。我们可以用这些信息模拟灯光的“闪烁”。
当一只萤火虫闪烁的时候，它也会用`||无线电：无线发送数字||`通过无线电来发送一个数字。

![](https://i.imgur.com/CT7afgv.png)

当一只萤火虫接收到无线电数据，并且它没有发送数据时，它会将其时钟时数加1：:

![](https://i.imgur.com/XhkPlK6.png)

### 完整代码

[https://youtu.be/XzZeB4yYnEw](https://youtu.be/XzZeB4yYnEw)

将这个程序下载到你所能找到的多块micro:bit上，并在暗处试一试吧！

注意：我们已经添加了一个`||无线电：无线设置组||`积木块来指定萤火虫将在哪个组进行通信。 

![](https://i.imgur.com/csCzzVV.png)

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_L8MLAyLRq4ms" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>
