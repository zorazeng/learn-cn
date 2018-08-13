## 微币

你听说过比特币或者所有这些新的加密货币吗？很好，现在micro:bit也有微币了哦！

### 如何用一块micro:bit制作硬币呢？

每块micro:bit包含了一个**区块链**，也就是一系列**积木块**。这些积木块使公共的，不能被修改。每个积木块代表了一枚**硬币**。为了挖掘更多新的硬币，用户摇晃micro:bit。如果他们幸运的话，他们的硬币会作为一个新的积木块添加到这个链条中哦！一旦这个积木块被添加，它就会展示给其他的micro:bit(这个区块链是公共的，不能修改，但是我们可以分享它）。其他的micro:bit收到这个积木块后，交易生效，并根据需要更新他们的积木块。 

按下按钮`A`，显示你添加到这个链条中的积木块的数量。这就是你的得分。按下按钮`B`，显示链条的长度。

尽情地淘金吧！

### 硬币、积木块、链条

一个*区块链*是一系列用于记录一种加密货币（例如：比特币）的交易的积木块。一个积木块可能包含的信息诸如：它被创造（被挖掘）的时间和挖掘它的人。 积木块最重要的部分是它的哈希值。这是一个特别的数值。它是由积木块列表中的最后一个积木块的信息与列表中倒数第二个积木块的哈希值组合而成。新的积木块包含了当前交易的信息和这个新的哈希值。新的积木块被添加到之前积木块的列表中。之后，这个列表被传输到加密货币的网络中。要篡改或伪造一个哈希值，让区块链的传输变得公开，是非常困难的（几乎不可能完成）。

创建一个属于你的micro:bit钱包，用它来装满你的硬币吧！

### 代码

代码中使用了无线电区块链代码库中的积木块。

- 点击**高级**，然后再点击**添加软件包**。
- 搜索**blockchain**，添加**radio-blockchain**。

![](https://i.imgur.com/cI3OlNr.png)

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_P2i7umFdPFiK" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>

### 区块链代码使如何工作的呢？

[无线电区块链](https://makecode.microbit.org/pkg/microsoft/pxt-radio-blockchain)代码库使用无线电在micro:bit之间传输积木块。你可以在此[https://github.com/microsoft/pxt-radio-blockchain](https://github.com/microsoft/pxt-radio-blockchain)阅读JavaScript的课程，了解这个代码库是的工作原理。想直接进入到区块链的代码？请看这个文件： 

[main.ts ](https://github.com/Microsoft/pxt-radio-blockchain/blob/master/main.ts)- 包含完整的区块链的JavaScript课程。阅读愉快!

