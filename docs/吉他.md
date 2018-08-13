## 吉他

根据这篇教程来制作一把micro:bit吉他吧！

[https://youtu.be/GYmdTFvxz80](https://youtu.be/GYmdTFvxz80)

### 时长

总共有5个活动。根据编程概念的熟悉程度，每个活动大约需要30-45分钟。

### 制作材料

- 大块的硬纸板
- 胶布
- 马克笔或者颜料
- 铝箔
- 剪刀
- 1块micro:bit、一个电池盒和2节7号电池
- 4-5个鳄鱼夹
- 耳机

### 活动

### 制作吉他的琴身

#### 制作材料

- 大块的硬纸板
- 胶布
- 马克笔或者颜料
- 剪刀

![](https://i.imgur.com/syKnyxK.png)

#### 步骤 1：设计琴身

吉他设计参考来源： [https://youtu.be/xMSrWaOZkFg](https://youtu.be/xMSrWaOZkFg)

- 搜索[吉他剪影](https://cn.bing.com/images/search?q=Guitar+Silhouettes)的设计理念，并自定义吉他的形状。
- 在平坦的纸板上追踪设计（最好是40-80厘米的硬纸板）。

- 忽略一些难以在硬纸板上裁剪出的部分
- 拆开一个纸盒以获得一个更长的纸板，并且可以增强折痕

#### 步骤 2：裁剪琴身

剪切硬纸板：[https://youtu.be/aUQkrFoEank](https://youtu.be/aUQkrFoEank)

#### 步骤 3：个性化吉他

用胶布、马克笔、颜料和其他可以用到的材料创作出不同的风格(你们都是艺术家哦！)

装饰吉他：[https://youtu.be/zNAZTJeSxY8](https://youtu.be/zNAZTJeSxY8)

每个人都可以创作出一个不同的设计哦!

![](https://i.imgur.com/mc84yAk.png)

#### 补充说明!

坚固吉他:[https://youtu.be/q0GkQdJmxjE](https://youtu.be/q0GkQdJmxjE)

用一个带角度的硬纸条来使吉他更加坚固。（可选）

### 按钮、显示&声音

#### 制作材料

1块micro:bit、一个电池盒和2节7号电池

![](https://i.imgur.com/ZYiLIDO.png)

2-4个鳄鱼夹

![](https://i.imgur.com/DEPBI1g.png)

耳机

![](https://i.imgur.com/j9d3Hcg.png)

#### 方块

![](https://i.imgur.com/2A8OxZy.png)

#### 步骤 1：制作一个笑脸

在浏览器中打开 [https://makecode.microbit.org/](https://makecode.microbit.org/)。

![](https://i.imgur.com/jZSIapF.png)

从**基本**中，将一个**显示LED**积木块拖拽到代码编辑区域，并用LED创作出一个表情。

![](https://i.imgur.com/RkPW6Fh.png)

用USB线将micro:bit连接至电脑，并点击`下载`。根据操作指引，将代码下载到micro:bit上。 

#### 步骤 2：添加笑脸LED按钮事件

![](https://i.imgur.com/FJOqZVf.png)

从**输入**中，将一个**当按钮A被按下**积木块拖拽到代码编辑区域。

- 将上面的显示LED积木块放入到这个积木块中。
- 创建一个**当按钮B被按下**积木块，并将另一个带有笑脸的`显示LED`积木块放入其中。
- 将代码下载到micro:bit, 并试着按下A、B按钮。

#### 步骤 3：用鳄鱼夹连接耳机

![](https://i.imgur.com/3yvOeDz.png)
![](https://i.imgur.com/dGKJdXJ.png)

用一个鳄鱼夹将**耳机插头的底端**连接到micro:bit上的**GND**引脚。

用另一个鳄鱼夹将**耳机插头的顶端**micro:bit上的**P0**引脚。

连接micro:bit和电池：[https://youtu.be/zwRTmpKIaVU](https://youtu.be/zwRTmpKIaVU) 
将micro:bit和电池组连接到吉他的琴身上。

连接耳机的扬声器：[https://youtu.be/ewyEW_U5G9M](https://youtu.be/ewyEW_U5G9M) 
用鳄鱼夹连接耳机

**micro:bit可以播放音乐**

**播放铃声**积木块可以播放从**C**到**B5**范围内的字母音调。用一连串音调组成一首歌，就像《生日快乐歌》的开头(C、C、D、C、F、E)。

![](https://i.imgur.com/H6XDeBj.png)

#### 步骤 4：给按钮A&B添加播放铃声事件

![](https://i.imgur.com/aOjxpwR.png)

从**音乐**中，将`播放音调C持续1拍`积木块拖拽出来，放到`当按钮A被按下`下方的 **显示LED**积木块中。

- 通过选择一个音符（字母）来修改**音调**，并体验一下高音和低音。
- 将**节拍**设置成1。

重复按钮B的事件
将代码下载到micro:bit
通电后，用耳机试一试AB两个按钮。

#### 祝贺你完成了吉他制作的基本步骤!

**挑战：** 给每个按钮创建更长的示例音乐，而不仅仅是单个音符。
**提示：** 搜索“ABC 音乐音调”或者“简易音乐音符”，以及一首歌的名称。

#### Extra

[笑脸](https://makecode.microbit.org/projects/smiley-buttons)
[改造耳机](https://makecode.microbit.org/projects/hack-your-headphones)

### 光传感器和音调控制

用光传感器来控制吉他弹奏的电子琴的音调。

概念：
- 输入
- 光强度
- 音调/频率
- 比率映射
- 无限循环
- 带有编程性质的数学（乘法）

时长：30 - 45分钟

用光传感器来演奏音调 [https://youtu.be/2cKg9pokVC4](https://youtu.be/2cKg9pokVC4)

#### micro:bit的LED光传感器

- micro:bit根据照射到LED屏幕的光线来检测外部的光线强度。
- 亮度级别积木块反应一个从0（黑暗）到255（明亮）的数值。
- 需要一个`无限循环`来持续检测当前的亮度级别和控制音调。 

#### 无限循环

`无限循环`真的是使代码永远运行。当有需要不断检查一个事件或者是在代码中使用一个变化中的数值，`无限循环`就变得非常有用了。

#### 方块

![](https://i.imgur.com/QPvfG7M.png)

#### 步骤 1：创建一个亮度等级检测器

![](https://i.imgur.com/zPnv5qA.png)

**搭建积木块** 
从`基本`中拖拽出一个`无限循环`积木块，放入到代码编辑区域。
从`LED`中拖拽出一个`绘制条形图`积木块，放入`无限循环`的下方。
从`输入`中拖拽出一个`亮度等级`积木块，放入到`绘制条形图`积木块中。

**将绘制条形图的值设置为最高 = 255**

#### 步骤 2：测试改变条形图高度所需要的亮度

绘制条形图的亮度输入：[https://youtu.be/pqU7bTcfQ_s](https://youtu.be/pqU7bTcfQ_s) （试着改变`绘制条形图`的最大值，看看它对条形图高度的影响）

**255是最大的亮度输入读数 **，试一试小于255的其他数字。**找到一个数值**使图像可以显示1-5根条形图。

#### 频率

**频率**的计量单位是Hz(赫兹），即每秒的循环或者是每秒的震动。一个正常人的耳朵可以检测到的频率范围是20Hz~20,000Hz。micro:bit和耳机一起生成能够被检测到的大概的输出范围是~50Hz - 6,000Hz。

**261Hz** 代表着一个C音调。

![](https://i.imgur.com/Px4fSxx.png)

**播放音调**积木块可以指定一个数字化的**频率**，通过用一个带有代表C的数值的**数字**积木块来改变字母**C** 的音调。

![](https://i.imgur.com/Ambj1W6.png)

#### 步骤 3：用数学积木块乘以频率

积木块 输入.当按钮被按下(按钮.A, () => { 音乐.播放音调(261 * 2, 音乐.节拍(节拍数.1/2)) })

    创建一个带有**数学**选项的**播放音调**积木块，用**乘法**积木块来设置**音调**。

#### 接下来

**添加**一个按钮**B**积木块，用一个2以外的数字来乘以**261**以达到设置音调的目的。

**将代码下载到micro:bit**

**测试乘以了 261Hz *C* 频率的声音**


#### 步骤 4：用亮度输入来控制频率
积木块
基本.永远(() => {
    音乐.播放音调(输入.亮度等级() * 25,音乐.节拍(节拍数.1/4))
})


创建一个`无限循环`，将一个`播放音调`积木块放入其中。

设置音调。使用乘法积木块将亮度等级输入乘以25或者试一试乘以大于或者小于25的其他数字。

测试吉他的亮度音调控制
用你的手盖住LED屏幕使micro:bit检测到的亮度发生变化，从而控制音调。

干得不错，这把吉他的声音很不错哦！

挑战：给亮度等级乘积模块创建一个变量，用按钮来改变亮度。（可选）


### 加速度计节拍控制

用加速度计来控制吉他的节奏
概念：重力加速度、X/Y/Z坐标节奏节拍映射图、绝对值

时长：30 - 45分钟

加速度计控制节奏：[https://youtu.be/kA0HpqCWsjs](https://youtu.be/kA0HpqCWsjs)

#### 方块

![](https://i.imgur.com/u7NQi7R.png)

#### 加速度计、重力和倾斜

micro:bit内置了一个**加速度**传感器。这个传感器可以测量施加在micro:bit主板上的力。在地球上，我们受到了将我们拉向地面的重力的影响。

[https://youtu.be/0SULoTKmkhI](https://youtu.be/0SULoTKmkhI)

当micro:bit屏幕朝上平放在桌面的时候，重力和micro:bit的Z轴对齐。

![](https://i.imgur.com/2V4b2io.png)

如果你将它向上或者向下倾斜，重力将会与Y轴对齐。这也就是我们检测倾斜的方法！如果沿着Y轴的力增加，micro:bit的倾斜将会变得更加垂直。 

#### 沿着不同的坐标轴（X/Y/Z轴)测量加速度

加速度积木块大概测量的是milli-g（毫克），也就是1g(克）的1/1000或者是1/1000的重力加速度。

#### 步骤 1：图像加速度

![](https://i.imgur.com/YgIHhXf.png)

**创建代码** 用于测量Y轴加速的的变化，并通过图像显示在LED屏幕上。
**下载代码**到micro:bit。
**测试LED屏幕上1-5个条形变化的运动**

##### 补充说明

试着沿着X轴和Z轴绘制加速度。你能解释它们的不同吗？

映射
将一个标准映射到另一个标准上是很常见的-例如：温度。
![](https://i.imgur.com/O2Kz8zB.png)

#### 步骤 2：将加速度映射到节奏上

micro:bit传感器生成的信号值是在0~1023之间。映射积木块会将信号转换成我们所需要的一个范围。 

![](https://i.imgur.com/tRUNsCh.png)

**创建代码** 将Y轴的加速度映射为节奏。
**下载代码**到吉他上的micro:bit。
**测试加快和减慢节奏的动作。**

#### 步骤 3：结合光传感器音调控制

将上面的步骤都结合起来吧！

![](https://i.imgur.com/ULSTL2b.png)

**将上述的代码和之前活动中的光传感器音调控制代码结合起来。**
**下载代码**到吉他上的micro:bit。
**现在，用光传感器和加速度计调节吉他的音调和节奏吧！**


### 按下引脚切换

用按下引脚来切换吉他的开关状态。

概念：
- 电路
- 导体
- 变量/全局变量
- 条件：if，else
- 布尔逻辑：True/False

时长：约45分钟 

#### 制作材料：
2-3个鳄鱼夹

#### 方块

![](https://i.imgur.com/Le5izGZ.png)

#### 电路&开关

- 电路需要电源（电池），电阻（如LED）和导体（金属，水，手）。
- 开关通过用导体闭合（完成）电路来接通电源，因而电可以流动。
**金属箔和金属丝是很好的导体。**

**在这项活动中，我们将通过人体来导电，从而闭合吉他的电路，实现吉他的开启和关闭状态的切换。**

#### 步骤 1：引脚按下测试

![](https://i.imgur.com/mZyeg3G.png)

**创建引脚按下代码**
**下载代码**到micro:bit上

[https://youtu.be/PAIU-vHqyGU](https://youtu.be/PAIU-vHqyGU)


拿起micro:bit, 用一只手按住GND引脚，另一只手选择性地按住P0、P1和P2其中一个引脚。
电路信号是通过引脚来传输的。micro:bit检测到的信号经过你的两只手，再传输到micro:bit的GND引脚。

#### 步骤 2：在吉他上安装导电金属箔

[https://youtu.be/NX0ECcpXFes](https://youtu.be/NX0ECcpXFes) 
在吉他琴身上添加金属箔，使其在弹奏时易于被触摸。

用鳄鱼夹将金属箔连接到micro:bit的`GND`引脚。

[https://youtu.be/YkymZGNmkrE](https://youtu.be/YkymZGNmkrE) 
在吉他琴颈上添加金属箔

用鳄鱼夹将金属箔连接到micro:bit的`P1`引脚。

#### 步骤 3: 添加吉他开关
用`on`这个全局变量，我们可以在micro:bit的开和关之间切换信息。

![](https://i.imgur.com/oGunEqt.png)

**创建开关的代码**
**将代码下载到micro:bit**
**通过触摸`P1`来测试LED屏幕在开和关状态下的信息切换**
最后需要编写的代码：在切换开关上，我们是想用 `on = !on`; 还是更直接一点的 `on = true; on = false;` ？

![](https://i.imgur.com/zvdT0ME.png)

#### 现在开始弹奏吉他吧!

用两只手同时触摸两块金属箔来接通开关的电路，并按下连接金属箔的引脚，来控制吉他的开关。

[https://youtu.be/GYmdTFvxz80](https://youtu.be/GYmdTFvxz80)






