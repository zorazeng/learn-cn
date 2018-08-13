## 香蕉键盘

用香蕉来创作你自己的micro:bit钢琴吧！

![](https://i.imgur.com/V2264co.png)

时长：~20分钟。

### 制作材料

- micro:bit、电池盒和2节7号电池
- 香蕉
- 橘子
- 4个鳄鱼夹

### 制作过程

#### 步骤 1 - 连接接地引脚

![](https://i.imgur.com/EIE1bXB.png)

拿出第一个鳄鱼夹，将鳄鱼夹的一端连接到micro:bit的接地引脚。

#### 步骤 2 - 连接声音引脚

![](https://i.imgur.com/xJN7jzv.png)
![](https://i.imgur.com/12kkChu.png)

拿出第二个鳄鱼夹，将鳄鱼夹的一端连接到micro:bit上的引脚P0。 

#### 步骤 3 - 耳机连接接地

![](https://i.imgur.com/Qb800F9.png)

将第一个鳄鱼夹的另一端连接到耳机插头的底端。

#### 步骤 4 - 连接耳机发声触点

![](https://i.imgur.com/XokJWQQ.png)
![](https://i.imgur.com/h60F0pB.png)

将第二个鳄鱼夹的另一端连接到耳机插头的顶端。

#### 步骤 5 - 连接水果的引脚

![](https://i.imgur.com/D5KoDzW.png)

拿出第三个鳄鱼夹，将鳄鱼夹的一端夹在第一个鳄鱼夹夹住micro:bit**GND**引脚的一侧。

#### 步骤 6 - 将橘子接地

![](https://i.imgur.com/05QKs9j.png)
![](https://i.imgur.com/9S9vYqZ.png)

将第三个鳄鱼夹未连接的另一端插入到橘子上。

#### 步骤 7 - 连接第二个水果引脚

![](https://i.imgur.com/0UvFF6G.png)

拿出第四个鳄鱼夹，将鳄鱼夹的一端连接到micro:bit上的引脚P1。

#### 步骤 8 - 连接香蕉

![](https://i.imgur.com/5c70v5z.png)

将第四个鳄鱼夹未连接的另一端插入到香蕉上。

#### 步骤 9 - 香蕉键盘完成

![](https://i.imgur.com/6mpf0N4.png)

你的香蕉键盘已经做好了！

#### 步骤 10 - 测试键盘

用USB线将你的micro:bit连接到电脑上并运行这个程序：

![](https://i.imgur.com/8zflVHS.png)

用一只手拿起橘子，用另一只手的手指敲打香蕉来发出声音。这样你的香蕉键盘就做好了！

### 代码

你是否曾经尝试着制作敲击盒子的声音？让我们尝试着用代码来制作这种声音，当然，还有一根香蕉哦！

#### 香蕉键盘代码

我们先添加一个变量来存储一个音符。将这个变量重命名为`sound`。将这个变量的数值设置到来自**音乐**抽屉音符积木块`中 A`。

![](https://i.imgur.com/5q4MStX.png)

我们想在拍打水果的时候演奏音乐。因此，我们使用了一个事件处理器，用于执行P1被按下的动作。当然，P1已经被连接到了香蕉上。从**输入**抽屉中，添加一个`当引脚被按下`积木块。

![](https://i.imgur.com/qGkySxI.png)

现在，让我们来创作一些音符。当我们拍打水果的时候，这些音符就会被演奏。点击**循环**抽屉，然后将一个`重复`循环插入到`当引脚被按下` 积木块中。点击**变量**抽屉，拖拽出一个`以幅度更改`积木块，并将它放入到循环中。将变量重命名为`sound`。将变量的值从`1`变为`25`。这将变量`sound`的`中 A`积木块音符频率增加到`中 A`加25，以此类推。在循环的末尾为`sound`添加一个`设置为`积木块。将`sound`设置为 `中 A`是为了在一次拍打香蕉之后重置声音。

![](https://i.imgur.com/8UGGCHz.png)

最后，在`设置为`的上方插入一个`播放音调`的积木块。将`sound`变量积木块拖拽出，并将它放在`播放音调`的音符凹槽内。将节拍变为`1/4`拍。

![](https://i.imgur.com/Xu6mUPh.png)

Click `下载` and try a banana press. Did you hear 4 notes play?

#### 添加另一个香蕉键盘

返回制作过程，用另一根香蕉重复步骤7和步骤8，但是这次的话是将鳄鱼夹连接到micro:bit上的引脚P3。

复制`当引脚被按下`时间处理器来生成另一个`当引脚被按下`。对于这个新的`当引脚被按下`，把引脚的名称改为**P2**。在引脚**P2**的事件中，将变量`sound`的频率改为减少25，而不是增加25。将`以幅度更改`积木块中的`25`改为`-25`。好了，你的代码现在看起来像这样：

![](https://i.imgur.com/UxrkVnF.png)

再次点击`下载`，并用这两根香蕉演奏。 这真是一个果酱节呀！

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_KhDPVcCpchVL" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>
