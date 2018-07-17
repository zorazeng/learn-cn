## 3.3 显示屏相关API ##
----------
### API ###
	
- 在之前 *2.4 什么是API* 小节中介绍过什么是API，MicroPython编程离不开API支持，下边就是5X5点阵显示屏可能涉及和使用到的API详细说明。

***注意：***某些方法的参数可以缺省表示。


| API | 描述 | 
| :------------: | :-----------: |
|`display.show(iterable, delay=400, wait=True, loop=False, clear=False)`|显示`iterable`中的每个图像或字母，每个显示之间延迟400ms`delay`，阻塞等待`wait`，不循环`loop`，不清屏`clear`。 |
|`display.show(image, delay=0, wait=True, loop=False, clear=False)`|显示一个内置图像`image`，每个显示之间延迟0ms`delay`，阻塞等待`wait`，不循环`loop`，不清屏`clear`。|
|`display.scroll(string, delay=400)`|在显示屏上滚动一个字符串`string`，延时`400`ms`delay`。|
|`display.get_pixel(x, y)`|获取`(x，y)`位置的亮度，亮度范围为0(关闭)到9(最亮)。
|`display.set_pixel(x, y, val)`|设置`（x，y）`位置的亮度为`val`（介于0 [关闭]和9[最亮]之间）。
|`display.clear()`|清空屏幕。|

### microbit内置图像 ###
- MicroPython中内置了很多有趣的图片，以点阵的显示显示。
- 如下列表截取了一部分图片名称，如需获取完整列表请链接：[Micro:bit官方参考文档](http://microbit-micropython.readthedocs.io/en/latest/tutorials/images.html)


Image.HEART : 爱心<br>
Image.HEART_SMALL ：爱心（小）<br>
Image.HAPPY ：开心<br>
Image.SMILE ：微笑<br>
Image.SAD ：难过<br>
Image.YES ：对<br>
Image.NO ：错<br>
...... <br>
