## 2.2 MicroPython中的程序结构 ##
----------

- 上一节`Hello World`程序已经烧录到Micro:bit板子中，并且完成相应的代码功能,现在我们来分析一下这段代码中具体做了什么。


```Python
	from microbit import * 
		display.scroll("Hello, World!")
```


1. 第一行代码：`from microbit import *`

	- 这行代码的意思是：我需要获得MicroPython的所有东西，我们需要“`from`(来自)”“`microbit`(代码库)”的东西，具体需要“`import`(导入)”“`*`(所有文件)”
	- 总体来说：**导入MICROBIT代码库所有的文件。**
	- 为了给Micro:bit上的模块编程，每一个MicroPython程序都需要导入MICROBIT代码库，以后用到的其他外部扩展模块也同样需要导入相应的代码库。
2. 第二行代码：`display.scroll("Hello, World!")`
	
	- 这样代码的意思是：“`display`(显示)”“`scroll`(滚动显示)”“`(Hello, World!)`(显示内容)”
	- 总体来说：**滚动显示“Hello, World!”。**

- MicroPython的运行方式是解释性运行，从上之下逐条运行，每一行代码都可以解释成需要完成的工作，代码简洁易懂。
- 当代码运行到最下边一条，意味着程序的结束。
- 接下来我们详细的分析代码中的每一个单词的具体用法。 


