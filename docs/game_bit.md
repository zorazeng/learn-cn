## 简介
---
Game:bit 是为micro:bit量身定做的游戏手柄，主板上有一个操纵杆；四个自定义按键；以及声音和震动反馈。同时它兼备主板取出断电、插入通电功能，节能且便利。用它控制小车行动，体验编程的无限乐趣。

![](https://i.imgur.com/XRAYD5N.jpg)  

## 特性
---
- 板载蜂鸣器。
- 板载震动反馈。
- 拔出主板自动断电。
- 引出7路扩展IO口。

## 参数
---
|项目|参数|
|:-:|:-:|
|电压|DC 3V|
|供电方式|2 X AAA电池|
|摇杆数量|1个|
|自定义按钮|4个|
|蜂鸣器|支持|
|震动反馈|支持|
|尺寸|109.61mm X 49.56mm|
|净重|31.3g|

## 外形与安装定位尺寸
---

![](https://i.imgur.com/cEMB6uA.png)  

## 主体功能模块介绍
---
### 摇杆   
![](https://i.imgur.com/16Na1x6.png)  
摇杆的X轴与Y轴分别连接在micro:bit 的P1与P2口。

### 蜂鸣器   
![](https://i.imgur.com/NZOy696.png)  
蜂鸣器为无源蜂鸣器，连接在micro:bit的P0口。

### 震动马达  
![](https://i.imgur.com/3wVSHD5.png)  
震动马达连接在micro:bit的P16口。

### 按键  
![](https://i.imgur.com/b1wuw5f.png)  
C、D、E、F四个按键分别连接在micro:bit的P12、P13、P14、P15口。

### 7个GVS接口  
![](https://i.imgur.com/JZshFRv.png)  
7个GVS扩展接口，可自行焊接排针进行扩展。

## 快速上手
---
### 安装
将两节AAA电池装入game:bit,并插入micro:bit主板。

### 添加game:bit package
进入[makecode](https://makecode.microbit.org/)在线编程平台，新建项目后，点击`Extensins`进入添加package的页面。
![](https://i.imgur.com/OEhaqWr.png)  

搜索关键词`gamebit`,添加 game:bit package。
![](https://i.imgur.com/Th0J0D4.png)  

![](https://i.imgur.com/8Cts0YA.png)  


![](https://i.imgur.com/F02lFh7.png)  

代码连接：[https://makecode.microbit.org/_Wa2JYxbWa2m1](https://makecode.microbit.org/_Wa2JYxbWa2m1 "https://makecode.microbit.org/_Wa2JYxbWa2m1")

你可能通过以下网页直接下载程序：

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_U8g12ia1PE6g" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>

下载完成后，打开电源开关：
可以听到开机声音  
按下C键：手柄震动一下  
按下D键：手柄震动一下  
按下E键：手柄震动一下  
按下F键：手柄震动一下  

## 文档
---

## 常见问题
---





