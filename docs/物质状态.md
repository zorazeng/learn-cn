## 物质状态

一起来制作一个可以响应你的micro:bit魔棒或micro:bit的运动的物质状态的实验吧！

[https://youtu.be/Hdsy93yaQC0](https://youtu.be/Hdsy93yaQC0)

### 时长

基于对编程概念的熟悉程度，这个活动大约需要30-45分钟。

### 材料

- 硬纸板
- 铝箔
- 永久记号笔（红色和黑色）
- 1块micro:bit、电池盒和2节7号电池
- 4个鳄鱼夹

### 活动

将一块硬纸板变为一个探测温度和气温的探测器吧！

[https://youtu.be/Hdsy93yaQC0](https://youtu.be/Hdsy93yaQC0)

- 将铝箔折成方块放在硬纸板四周。
- 将每片铝箔连接到micro:bit上对应的引脚。

这就是我们的探测器了！

### 代码

你是否曾经尝试着去展示物质的状态？让我们试着以直观的方法来展示基于气温的各种物质的状态吧！

#### 步骤 1：变量

为了让物质的状态遵循决定气温的规则，我们需要添加变量来存储数据。然后，给变量赋值。将2个变量命名为：“atmos_temperature” 和“temperature”。将变量的值设置为100。修改你的代码，让它看起来像这样：

![](https://i.imgur.com/hwjdtSI.png)

#### 步骤 2：检测固体

我们想要检测固体状态发生的时间。当引脚P2被按下时，我们想让micro:bit显示气温为0，并滚动显示一条信息“SOLID”。因此，我们需要将 atmos_temperature设置为0并显示字符串“SOLID”。修改你的代码，让它看起来像这样：

![](https://i.imgur.com/XQgEngn.png)

#### 步骤 3：检测液体

我们想要检测液体状态发生的时间。当引脚P1被按下时，我们想让micro:bit显示气温为80，并滚动显示一条信息“LIQUID”。因此，我们需要将 atmos_temperature设置为80并显示字符串“LIQUID”。修改你的代码，让它看起来像这样：

![](https://i.imgur.com/X2JXMg3.png)

#### 步骤 4：检测气体

我们想要检测物质变为气体的时间。当引脚P0被按下时，我们想让micro:bit显示气温为250，并滚动显示一条信息“GAS”。因此，我们需要将 atmos_temperature设置为250并显示字符串“GAS”。修改你的代码，让它看起来像这样：

![](https://i.imgur.com/IA4WT70.png)

- 点击下载，看看代码是否有效。

#### 步骤 5：增加温度

我们想要在摇晃micro:bit的时候显示温度的变化。当你摇晃的时候，micro:bit会显示一个图标来代表温度增加。修改你的代码，添加摇晃事件： 

![](https://i.imgur.com/O3prPEa.png)

- 点击下载，看看代码是否有效。

#### 步骤 6：显示温度变化

我们想根据一个布尔条件是true或false，有条件地运行代码。我们想让micro:bit在摇晃的时候显示特定的图标来反应温度的变化。我们将会创建两个条件语句。在显示了一个图标之后，用`清空屏幕`将这个图标从屏幕上清除。然后，我们将暂停运行程序100毫秒。这个函数有助于降低程序运行的速度。

第一个条件语句遵循这个逻辑：
- 如果温度低于气温，将温度增加20。 
- 如果温度不低于气温，将温度减少20。

第二个条件语句遵循这个逻辑：
- 如果温度低于32度，显示一个代表固体的图标。
- 如果温度低于212度，显示一个代表液体（雨伞）的图标。
- 如果温度大于或等于212度，显示一个代表气体的图标。

![](https://i.imgur.com/uZKbSDG.png)

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_AcmHMpARYggq" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>







