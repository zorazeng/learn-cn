## 牛奶怪兽

一起来制作一个有趣的牛奶怪兽吧！

[https://youtu.be/egl3fNAYylk](https://youtu.be/egl3fNAYylk)

### 时长

3个活动。根据编程概念的熟悉程度，每个活动大约30-45分钟。

## 材料

### 回收物

- 1个牛奶纸盒（带一个可拧顶盖）
- 1根从用过的茶包上回收而来的绳子
- 1个回形针

### 电子元件

- 1块micro:bit、电池盒和2节7号电池
- 3个鳄鱼夹
- 1个迷你舵机9g SG90
- 1个为牛奶怪兽设计的舵机夹子，购买自thingiverse（可选）。老师们可能更喜欢购买课堂用的组件（16个舵机夹子）。

### 工具

- 小刀或剪刀（用于切割硬纸板）
- 胶布
- 胶枪

![](https://i.imgur.com/LfAhxnU.png)

### 准备工作

- 用鳄鱼夹夹住舵机
- 切割模型
- 购买或用3D打印打印出thingiverse为牛奶怪兽专门设计的舵机夹子。（可选）老师们可能更喜欢购买课堂用的组件（16个舵机夹子）。


## 活动

### 制作

将一个牛奶纸盒变为一个牛奶怪兽吧！

![](https://i.imgur.com/MP5tMLT.png)

时长：~45分钟

### 步骤 1：下载并剪切模板

[下载模板](https://makecode.trafficmanager.cn/blob/79ae8fdb5327e7dc76cdb94ca38434e4559cba4c//static/mb/projects/milky-monster/template.pdf)并切割模板。

[https://youtu.be/ipsZuFNgTHM](https://youtu.be/ipsZuFNgTHM)

### 步骤 2：粘贴模板

将模板粘贴到牛奶盒子上。

[https://youtu.be/2D3WFp29QC4](https://youtu.be/2D3WFp29QC4)

### 步骤 3：切割纸盒

切割纸盒（注意别伤到手指！）

[https://youtu.be/pvC3Tnhe5QU](https://youtu.be/pvC3Tnhe5QU)

### 步骤 4：制作嘴巴

剪切出硬纸板的中部，并把角折好。这将会是牛奶怪兽的嘴巴。

[https://youtu.be/Yyk1zW4sFoM](https://youtu.be/Yyk1zW4sFoM)

### 步骤 5：延长嘴巴

用胶布将嘴巴延长约1cm。将胶布的一边折叠到另一边的后面。

[https://youtu.be/RWJbqI03wPE](https://youtu.be/RWJbqI03wPE)

### 步骤 6：接线

用剪刀剪出一个小孔，把绳子插入小孔。用胶布将线粘在怪兽的嘴巴后面。

![](https://i.imgur.com/NH2LLUL.png)

完成后，将怪兽的嘴巴朝上放置，把刚才的绳子穿过牛奶盒顶部的盖子。

[https://youtu.be/Qyndcsmt0AU](https://youtu.be/Qyndcsmt0AU)

### 步骤 7：给micro:bit创造空间

用剪刀在牛奶怪兽的底部剪出一个空间，用于粘贴micro:bit。

[https://youtu.be/3FUNI0GSbNc](https://youtu.be/3FUNI0GSbNc)

### 步骤 8：给线创造空间

在牛奶怪兽后面剪切出一个小孔，用来藏好线。

[https://youtu.be/BoIRCk769MM](https://youtu.be/BoIRCk769MM)

### 步骤 9：将回形针连接舵机 

用一个十字螺丝刀将舵机固定到3D打印的舵机夹子上。如果你没有3D打印的舵机夹子，在[thingiverse](https://www.thingiverse.com/thing:2185971)下载，或用扎带或胶枪将舵机固定住。 

[https://youtu.be/drKzo5zqvuI](https://youtu.be/drKzo5zqvuI)

### 步骤 10: 将舵机粘贴到牛奶盒的盖子上

用胶枪将舵机粘在牛奶盒的盖子上。

[https://youtu.be/Ch_vU5LXPeM](https://youtu.be/Ch_vU5LXPeM)

### 步骤 11：在盖子上切孔

在盖子上切出一个小孔，将线引导到舵机上。

[https://youtu.be/JKi2Ns8y3nI](https://youtu.be/JKi2Ns8y3nI)

### 步骤 12: 连接鳄鱼夹

将鳄鱼夹连接到舵机。

[https://youtu.be/RiQE-9z9LrI](https://youtu.be/RiQE-9z9LrI)

### 制作完成

牛奶怪兽已经制作完成，是时候该装饰一下它了！将这个牛奶怪兽改造成你喜欢的风格吧！

![](https://i.imgur.com/BI6tpRF.png)

## 代码

添加代码让牛奶怪兽动起来。
时长：~30 分钟

### 步骤 1：舵机校准

为了让牛奶怪兽动起来，micro:bit需要给舵机指令，让舵机以一定的速度在`0`度和`180`度之间转动。指令代码如下： 

- 按下按钮`A`将舵机旋转到180度（合上牛奶怪兽的嘴巴）。
- 按下按钮`B`将舵机旋转到0度（张开牛奶怪兽的嘴巴）。

![](https://i.imgur.com/3VyDtt4.png)

### 步骤 2：安装摆臂

在安装摆臂**之前**，舵机应固定在180度。当舵机达到180度，这将确保牛奶怪兽的嘴巴是合上的。
你可以用十字螺丝刀将摆臂安装到舵机上。

[https://youtu.be/YZfkMWTeH4o](https://youtu.be/YZfkMWTeH4o)

### 步骤 3：检查校准

当使用者按下按钮`A`，舵机摆臂会处于“向上”的位置。

[https://youtu.be/bAqXEawUsSM](https://youtu.be/bAqXEawUsSM)

### 步骤 4: 将线连接到摆臂上

当牛奶怪兽的嘴巴合上的时候，将绳子连接到舵机的摆臂上。

[https://youtu.be/AWsnwk_iA_A](https://youtu.be/AWsnwk_iA_A)

### 步骤 5：将线连接到micro:bit

用micro:bit上引出的线连接舵机，并将电池组连接到micro:bit。

[https://youtu.be/fAR58GJUZdM](https://youtu.be/fAR58GJUZdM)

### 步骤 6: 给光传感器编程

在micro:bit上给光传感器编程来控制舵机。

![](https://i.imgur.com/0bX1NyV.png)

### 步骤 6：完成

你的牛奶怪兽已经做好了！

[https://youtu.be/egl3fNAYylk](https://youtu.be/egl3fNAYylk)

##### 完整代码：
![](https://i.imgur.com/RJTPgvM.png)

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_5RhMkP9ccXRP" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>


## 连接

用另一块micro:bit来遥控你的牛奶怪兽。
时长：~30分钟
这里，你将用到第二块micro:bit。通过使用无线电，我们可以用另一块micro:bit来控制牛奶怪兽。将下面的代码下载到牛奶怪兽上的micro:bit和另一个“控制器”micro:bit。无论按钮`A`何时被按下，牛奶怪兽将移动一次。

![](https://i.imgur.com/OvvwtU3.png)






