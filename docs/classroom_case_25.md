## 剪刀石头布小组



一起来玩多人版剪刀石头布吧！



[https://youtu.be/8ztOmdZi5Pw](https://youtu.be/8ztOmdZi5Pw)



剪刀石头布通常是一个双人游戏，但是它也可以是一个多人游戏哦！当玩家人数超过两个的时候，它就变成了一个小组游戏：所有玩家同时摇晃micro:bit，然后记录所有玩家的剪刀、石头、布的数量。玩家数量最多的一组获胜。



从基础版的剪刀石头布游戏开始，我们将改变代码让micro:bit统计并显示同一组玩家的数量。micro:bit将通过无线电通信来发送它的状态，并接收其他micro:bit的状态。



让我们开始吧！



### 起始积木块



让我们先编写双人版游戏的代码。双人版的游戏选择了一个`||输入：当振动||`事件中的一个工具，并显示一个相对应的图标。看看下面的代码，刷新你的记忆。



![](https://i.imgur.com/VhZhgnm.png)



#### 步骤 1：重新重组

**重构**在编程中是一个有趣的词，它的意思相当于`重组`。在这个案例中，我们将显示剪刀、石头、布的图标的代码移动到它自己的`||基本：无限循环||`的循环中。



![](https://i.imgur.com/FbE90cG.png)



#### 步骤 2：通过无线电发送状态 



将`tool`的值通过无线电发送到`||基本：无限循环||`循环中的另一块micro:bit上。因为无线电信号可能会到达或者不会到达，所以我们最好不断地发送无线电信号。



我们也设置了无线电组，发送了设备的序列号（micro:bit独立的身份识别的数字），我们稍后会用到它。



![](https://i.imgur.com/9E3G723.png)



#### 步骤 3：小组名单



所有玩家都在不断向其他玩家展示他们选择的工具。让我们添加接收这个状态的代码并对其进行计数。



我们将添加一个数组变量，其中包含与当前玩家在同一小组中的所有玩家。这个名为`players`的数组就像你的小组名单一样，它包含了和你使用了相同工具的micro：bit序列号列表。



![](https://i.imgur.com/ouQcbE9.png)



#### 步骤 4：接收信息（1）



在一个`||无线电：在无线接收到||`事件中，我们从另一块micro:bit上收到了状态。点击**齿轮**图标，添加`序列`参数，我们将用它来识别谁发送了信号。



我们从接收到的数据中计算出3个数值：



- `match`-一个布尔值，表明另一块micro:bit使用的工具是否和我们当前使用的工具一样。

- `player_index`-在其他micro:bit的序列号数组中的位置。如果它不在数组中，那么它将会是-1。

- `found`-一个布尔值，表明micro:bit的序列号是否在玩家的数组中。



![](https://i.imgur.com/ez1xZZU.png)



#### 步骤 5: 接收信息（2）



当考虑到`match`（匹配）和`found`（发现），我们需要处理两种情况：



- **如果** 我们有了一个`match`（匹配），但是玩家`非found`（不在）列表中，那么我们把它添加到`players`。

- **如果** 我们没有一个`match`（匹配），但是玩家`found`（在）列表中，那么我们把它从`players`中`移除`。



我们将上述两种情况放入到两个`||逻辑：如果 则||`语句中判断序列号是否被添加或者删除。 



![](https://i.imgur.com/lwG2NqG.png)



#### 步骤 6：重置小组



如果一些玩家离开了游戏怎么办呢？他们将停止展示他们的状态，但是依然会保留在我们玩家的列表中。为了避免这个问题，我们通过摇晃micro:bit来重置`players`数组。



![](https://i.imgur.com/oAkNUWb.png)



#### 步骤 7：显示小组得分



小组得分是该小组中玩家的数量。这也就是`players`数组的`长度`。我们在`无限循环`中添加一个`显示数字`积木块来显示这个数字。



![](https://i.imgur.com/TDkZmQk.png)



### 最后的代码



现在，是时候把我们程序的每个部分组合在一起。仔细检查所有的步骤并将它们的整合起来。最终，它看起来像下面的这个程序。将代码下载到micro:bit上，和你的朋友们一起来玩一玩这个游戏吧！ 



![](https://i.imgur.com/AjwrlGd.png)





<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_Hta9pRcYq0gD" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>
















