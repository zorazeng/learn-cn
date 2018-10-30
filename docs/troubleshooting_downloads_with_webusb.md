
# 解决WebUSB下载问题
---
- 无法成功连接micro:bit和 [ WebUSB ](https://makecode.microbit.org/device/usb/webusb)？让我们一起来解决吧！

## 步棸1：检查USB接线
---

确定micro:bit是否已通过USB线和电脑建立连接。连接成功后，你会看到命名为**MICROBIT**的硬盘。

![](https://i.imgur.com/Squ6KpH.png)

**如果你看到MICROBIT 硬盘，请直接进入步棸2**。

如果没有看到，请继续：

- 先确定USB线是可用的。

    你的USB线确定可用吗？如果不行，就换一根。有一些USB线只能充电而不能传输文件。

- 试一下电脑上其他的USB接口。

USB线没有问题，但是电脑上仍未显示**MICROBIT**硬盘？那或许是你的micro:bit有问题。如果您购买的是我们的产品，请联系我们的售后客服。

## 步棸2：检查固件版本
---

让我们检查一下micro:bit上的固件版本是否需要更新：

1.进入MICROBIT 硬盘。

2.打开 DETAILS.TXT 文件。


![](https://i.imgur.com/GB7LQBv.jpg)

3.找到version number（版本编号）那一栏，**Version: xxx**： 

![](https://i.imgur.com/CU5Ajdd.jpg)

如果version后面的编号是**0234, 0241, 0243**，你就需要更新micro:bit 上的[固件](https://makecode.microbit.org/device/firmware)，进入步棸3，按照升级指示进行升级。

如果version后面的编号是**0249, 0250** 或者更大的数字，你的固件版本是无误的，直接到步棸 4。

## 步棸3：固件版本升级
---

1.设定micro:bit为**MAINTENANCE Mode**（维护模式）。先把USB线从micro:bit上拔出，按住重置按钮并重新插上USB接线.当USB线接入后，就可以松开重置按钮了。现在你会看到命名为**MAINTENANCE** 的硬盘，之前的**MICROBIT**硬盘已经没有了，同时重置按钮旁的黄色LED灯会持续闪烁。

![](https://i.imgur.com/02zBjkk.gif)

2.下载firmware ZIP文件[点击此处下载文件](https://github.com/ARMmbed/DAPLink/releases/download/v0250/0250_release_package_682d8303.zip) 。

3.在下载的**0250-release-package-682d8303.zip**中找到 **0250-kl26z-microbit-0x8000.hex**文件。

4.拖动文件至**MAINTENANCE** 硬盘内。

5.文件复制时黄色LED灯会持续闪烁，复制完成后黄色LED灯会停止闪烁，micro:bit完成版本升级。现在命名为**MAINTENANCE**的硬盘会变更为以**MICROBIT** 命名的硬盘。

6.升级完成啦！你可以打开DETAILS.TXT 文件，检查固件版本是否和你复制过来的文件版本一致。

_如果你想了解更多micro:bit主板连接，维护模式及固件升级等，可以访问[Firmware support page](https://support.microbit.org/support/solutions/articles/19000019131-how-to-upgrade-the-firmware-on-the-micro-bit) 了解更多相关信息_

## 步棸4：检查浏览器版本
---

WebUSB是全新功能可能需要更高版本的浏览器才能使用。检查一下你的浏览器是否为如下版本：

- Chrome 65+ for Android, Chrome OS, Linux, macOS and Windows 10。

## 步棸5：设备配对
---

当你完成固件升级后，打开谷歌浏览器进入make code编辑器页面，点击设置按钮，点击**设备配对**，可浏览[ WebUSB ](https://makecode.microbit.org/device/usb/webusb)的匹配说明。

享受飞速下载吧！
