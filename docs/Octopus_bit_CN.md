## 简介  
---

ELECFREAKS Octopus:bit是一款micro:bit的扩展板。它扩展出了micro:bit的GPIO口、串口、IIC接口、SPI接口。它最大的特点是可对部分GPIO口的工作电压进行电平转换，使micro:bit能适配5V的传感器。

![](https://i.imgur.com/wcgxnG0.png)


## 包装清单  
---

1 x ELECFREAKS Octopus:bit  


## 硬件  
---

### 特点  

- 输入电压3.3V（通过micro:bit边缘连接器供电）  
- 扩展了从P0至P16的PGIO口。  
- 每个I/O口下方都有VCC与GND的排针，并且用不同的颜色区分开来，用你可以很方便的连接你的扩展模块，该针脚的排布与章鱼系列完全兼容。  
- 具备升压模块，P8、P9、P11~P16的工作电平可通过电平转换开关在3.3V与5V之间切换。  
- 引出了串口、I2C接口与SPI接口，其中，I2C接口可以接3路I2C设备，SPI接口可以接两路SPI设备。  
- 两块扩展板之间可直接对接进行串口通信。  


## 应用  
---

适用于所有需要使用micro:bit GPIO的场景，如编程教育、制作智能设备等。  


## 引脚接口框图  
---

![](https://i.imgur.com/wCWdoag.jpg)


## 部分引脚接口详细介绍
---

### 标准GVS接口

![](https://i.imgur.com/gk3dN4E.png)

标准GVS接口，其中黄色部分（P0~P7， P10）工作电压为3.3V，蓝色部分（P8, P9, P11~P16）工作电压可通过电平转换开关在3.3V与5V之间切换。
每个I/O口下方都有VCC与GND的排针，并且用不同的颜色区分开来，用你可以很方便的连接你的扩展模块，该针脚的排布与章鱼系列完全兼容。

### 电平转换开关

![](https://i.imgur.com/JoxT6k2.png)

该开关可对蓝色部分IO口（P8, P9, P11~P16）的工作电平进行3.3V/5V切换。

该开关的作用范围如下图所示：
![](https://i.imgur.com/GHPffMl.png)

### 串口

![](https://i.imgur.com/8aVYsja.png)

串口的工作电压可通过电平转换开关进行3.3V/5V切换。
TX连接在P8，RX连接在P12，左边排针的部分为输入输出双向串口，右边排母为单向输出串口
**注意** 要使用该串口，请先按照如下程序初始化串口：

![](https://i.imgur.com/1gnuYd5.png)

## 外形与安装定位尺寸
---

![](https://i.imgur.com/ZYrWREG.jpg)


## 软件
---

## 示例1 播放音乐
---

### 硬件连接

将无源蜂鸣器模块连接至PO口。

![](https://i.imgur.com/Zc6ChwR.jpg)

### 示例代码  

![](https://i.imgur.com/0MBprkk.png)

代码连接：[https://makecode.microbit.org/_fAmC3WERHdR2](https://makecode.microbit.org/_fAmC3WERHdR2)  

下载完程序后，蜂鸣器将循环播放生日快乐歌。


## 相关案例  
---  

[Music Machine](https://www.elecfreaks.com/learn-en/Micro_bit_Tinker_Kit_Case_01_Music_Machine/)  
[Smart Light ](https://www.elecfreaks.com/learn-en/Micro_bit_Tinker_Kit_Case_02_Smart_Light/)  
[Electro-Theremin](https://www.elecfreaks.com/learn-en/Micro_bit_Tinker_Kit_Case_03_Electro_Theremin/)  
[Simple Alarm Box](https://www.elecfreaks.com/learn-en/Micro_bit_Tinker_Kit_Case_04_Simple_Alarm_Box/)  
[Plant Monitoring Device](https://www.elecfreaks.com/learn-en/Micro_bit_Tinker_Kit_Case_05_Plant_Monitoring_Device/)  
[Intruder Detection](https://www.elecfreaks.com/learn-en/Micro_bit_Tinker_Kit_Case_06_Intruder_Detection/)  
[Fish Feeder](https://www.elecfreaks.com/learn-en/Micro_bit_Tinker_Kit_Case_07_Fish_Feeder/)  
[Motion Detector](https://www.elecfreaks.com/learn-en/Micro_bit_Tinker_Kit_Case_08_Motion_Detector/)  
[Lie Detector](https://www.elecfreaks.com/learn-en/Micro_bit_Tinker_Kit_Case_09_Lie_Detector/)  
[PADDLEBALLSUPERSMASHEM](https://www.elecfreaks.com/learn-en/Micro_bit_Tinker_Kit_Case_10_PADDLEBALLSUPERSMASHEM/)  
[Avoid Asteroids](https://www.elecfreaks.com/learn-en/Micro_bit_Tinker_Kit_Case_11_Avoid_Asteroids/)  
[Remote Control Everything ](https://www.elecfreaks.com/learn-en/Micro_bit_Tinker_Kit_Case_12_Remote_Control_Everything/)  
[micro:bit Car](https://www.elecfreaks.com/learn-en/Micro_bit_Tinker_Kit_Case_13_Micro_bit_Car/)  
[Flipping Pancakes](https://www.elecfreaks.com/learn-en/Micro_bit_Tinker_Kit_Case_14_Flipping_Pancakes/)  
[Maze Runner](https://www.elecfreaks.com/learn-en/Micro_bit_Tinker_Kit_Case_15_Maze_Runner/)   
[QUICK MATHS](https://www.elecfreaks.com/learn-en/Micro_bit_Tinker_Kit_Case_16_QUICK_MATHS/)  
[Pitch Perfect](https://www.elecfreaks.com/learn-en/Micro_bit_Tinker_Kit_Case_17_Pitch_Perfect/)  
[Finger Dexterity](https://www.elecfreaks.com/learn-en/Micro_bit_Tinker_Kit_Case_18_Finger_Dexterity/)  
[Electric Spirit Level](https://www.elecfreaks.com/learn-en/Micro_bit_Tinker_Kit_Case_19_Electric_Spirit_Level/)   
[Space Shooter](https://www.elecfreaks.com/learn-en/Micro_bit_Tinker_Kit_Case_20_Space_Shooter/)  
[Flappy Bird](https://www.elecfreaks.com/learn-en/Micro_bit_Tinker_Kit_Case_21_Flappy_Bird/)  
[Wire Transmission](https://www.elecfreaks.com/learn-en/Micro_bit_Tinker_Kit_Case_22_Wire_Transmission/)  
[Snake Game](https://www.elecfreaks.com/learn-en/Micro_bit_Tinker_Kit_Case_23_Snake_Game/)  


## 相关配件
---  

### [BBC micro:bit](http://www.elecfreaks.com/estore/bbc-micro-bit-board-for-coding-programming.html)  

[![](https://i.imgur.com/nKomLk2.png)](http://www.elecfreaks.com/estore/bbc-micro-bit-board-for-coding-programming.html)  

### [Octopus电子积木系列](http://www.elecfreaks.com/estore/octopus-bricks-sensor)  

[![](https://i.imgur.com/m1Xdqvg.png)](http://www.elecfreaks.com/estore/octopus-bricks-sensor)  

### [ElecFreaks Micro:bit Tinker Kit](http://www.elecfreaks.com/estore/elecfreaks-micro-bit-tinker-kit.html)  

[![](https://i.imgur.com/pkfhaWF.jpg)](http://www.elecfreaks.com/estore/elecfreaks-micro-bit-tinker-kit.html)  


