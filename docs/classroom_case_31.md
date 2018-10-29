## 指南针

欢迎来到本节课程！这篇指导教程将向你展示如何编辑一个程序脚本来显示micro:bit所指的方向。让我们开始学习吧！

![](https://i.imgur.com/uH9kHQH.png)

用指南针来显示micro:bit所朝的方向。

### 步骤 1

创建一个循环，持续更新指南针的读数。 

![](https://i.imgur.com/Gv2jjiJ.png)

### 步骤 2

将micro:bit的读数存储在一个叫做`degrees`（角度）的变量中。

![](https://i.imgur.com/TigTtHi.png)

### 步骤 3

如果`degrees`小于`45`或者大于`315`，那么指南针大部分朝向**北**。在micro:bit上显示`N`。

![](https://i.imgur.com/hgRdEAe.png)

### 步骤 4

如果`degrees`小于`135`， micro:bit大部分朝向**东**。在micro:bit上显示`E`。

![](https://i.imgur.com/nNKkD1R.png)

### 步骤 5

如果`degrees`小于`225`，micro:bit大部分朝向**南**。 在micro:bit上显示`S`。

![](https://i.imgur.com/DBHmTve.png)

### 步骤 6

如果这些条件没有一个返回true（真），那么micro:bit一定是指向**西**。在micro:bit上显示`W`。

![](https://i.imgur.com/rLpwJxo.png)

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_EFPgi3ejUMEr" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>







