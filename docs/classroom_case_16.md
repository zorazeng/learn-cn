## 自动浇花

一起来制作一个自动浇花装置吧！

[https://youtu.be/7eC_VjH1eP0](https://youtu.be/7eC_VjH1eP0)

## 材料
---
- 1块micro:bit带电池盒和电池
- 2根长钉
- 2个鳄鱼夹
- 1个小舵机+ 3个母头鳄鱼夹
- 1根冰棍木棒
- 2根皮筋
- 1卷透明胶布
- 1根吸管
- 1把剪刀

## 活动
---

### 设置

#### 浆

根据视频中的操作指引，用micro:bit和一个舵机创建一个迷你水浆。

[https://youtu.be/jANCdtkJAKY](https://youtu.be/jANCdtkJAKY)

#### 土壤湿度传感器

根据土壤湿度项目中的操作指引，制作一个土壤湿度传感器，将代码下载到你的micro:bit上。

这是接线完成后的样子：

![](https://i.imgur.com/kMxxo8N.png)

### 代码

让我们添加一些代码，这样当土壤湿度等级低的时候，舵机就给植物浇水。

从土壤湿度项目中，我们知道当`reading`小于`500`的时候，土壤的湿度较低。我们可以用这个数字在代码中添加一个如果`reading < 500`来检测一个干燥的条件。

![](https://i.imgur.com/6isO3jZ.png)

舵机连接P2引脚，因此我们可以用`||向伺服引脚写入||`积木块来改变舵机的角度。我们想让角度变为`0`，直到水浇完后，然后再把角度返回到`80`。

![](https://i.imgur.com/xvo5pp7.png)

将上述代码插入到`无限循环`积木块的下方来循环检测土壤湿度。 

![](https://i.imgur.com/A81eGja.png)

这里有一个用micro:bit给植物浇水的视频。

[https://youtu.be/7eC_VjH1eP0](https://youtu.be/7eC_VjH1eP0)


<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_0wfdy5AovfUU" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>
