## Karel LED

一起来帮助Karel制作LED艺术品！
卡莱尔的的LED不能右转，但是他可以制作一些非常棒的LED艺术品哦！

![](https://i.imgur.com/uNU3GbH.png)

这个活动的目标是将下面给出的JavaScript代码下载到一块micro:bit上。然后，用这个程序给新学生介绍micro:bit。这次，学生们不用编程。他们将是熟悉micro:bit的用户。

### 如何玩

- `按钮A`**左转**

Does not draw anything just changes the direction Karel (the flashing led) is facing

- `按钮B`**向前移动**

将Karel向前移动一步并使他身后的LED灯保持点亮。

- `摇晃`**跳跃**

将Karel向前移动一步并关闭他身后的LED灯。

- `按钮A+B`**隐藏Karel**

显示或隐藏Karel(闪烁的LED灯）。当你的作品完成后，它只会被使用一次。

- `复位按钮`**清空屏幕并重启**

重新启动程序并清空屏幕。

**注意：** 除了重启，没有别的方法来清屏。

### 试着绘制一些图案

看看你能否用**按钮A**、**按钮B**和**摇晃**来制作下面的图案。当你完成了一次挑战，同时按下**按钮A**和**按钮B**来隐藏Karel。对于你设计的图案，思考你想点亮哪些LED灯，然后和Karel一起制作它。

#### 旋转

![](https://i.imgur.com/5kJdFzu.png)

#### 右转

![](https://i.imgur.com/MTZJPL0.png)

#### 眼睛

![](https://i.imgur.com/hyn6Tof.png)

#### 笑脸

![](https://i.imgur.com/DCbEArE.png)

#### 检查

![](https://i.imgur.com/adNXhyZ.png)


### 名字的首字母

思考如何用LED来生成你名字的首字母。

![](https://i.imgur.com/41EqXxr.png)

### 设计完成

祝你玩得愉快！

![](https://i.imgur.com/G3bJYEO.png)

感谢你用LED灯玩Karel!

## 编程

将这段代码复制粘贴到JavaScript编辑器中，然后将它下载到micro:bit上。
**注意:** 对于这个项目，你需要手动复制代码，将其插入到JavaScript编辑器中。

    /**
     * Karel the LED
     */
    basic.forever(() => {
    if (board.isKarelActive) {
    led.toggle(board.karelX, board.karelY)
    basic.pause(500)
    }
    })
    input.onButtonPressed(Button.A, () => {
    board.pressedA();
    updateLeds();
    })
    input.onButtonPressed(Button.B, () => {
    board.pressedB();
    updateLeds();
    })
    input.onGesture(Gesture.Shake, () => {
    board.shake();
    updateLeds();
    })
    input.onButtonPressed(Button.AB, () => {
    board.pressedAB();
    updateLeds();
    })
    function updateLeds() {
    for (let j = 0; j < 5; j++) {
    for (let k = 0; k < 5; k++) {
    if (board.ledState[j][k]) {
    led.plot(k, j);
    } else {
    led.unplot(k, j);
    }
    }
    }
    }
    const board = new Board();
    enum Direction {
    UP = 0,
    LEFT,
    DOWN,
    RIGHT
    }
    class Board {
    public isKarelActive: boolean;
    public karelX: number;
    public karelY: number;
    
    public ledState: Array < Array < boolean >>;
    private karelDirection: Direction;
    
    constructor() {
    this.isKarelActive = true;
    this.karelX = 2;
    this.karelY = 2;
    this.karelDirection = Direction.UP;
    this.ledState =[];
    for (let i = 0; i < 5; i++) {
    this.ledState.push([false, false, false, false, false]);
    }
    }
    
    pressedA() {
    if (!this.isKarelActive) {
    return;
    }
    this.karelDirection = (this.karelDirection + 1) % 4;
    }
    
    pressedB() {
    if (!this.isKarelActive) {
    return;
    }
    this.ledState[this.karelY][this.karelX] = true;
    this.moveKarel()
    }
    
    shake() {
    if (!this.isKarelActive) {
    return;
    }
    this.moveKarel()
    }
    
    private moveKarel() {
    if (!this.isKarelActive) {
    return;
    }
    switch (this.karelDirection) {
    case Direction.UP:
    if (this.karelY > 0) {
    this.karelY -= 1;
    }
    break;
    case Direction.LEFT:
    if (this.karelX > 0) {
    this.karelX -= 1;
    }
    break;
    case Direction.DOWN:
    if (this.karelY < 4) {
    this.karelY += 1;
    }
    break;
    case Direction.RIGHT:
    if (this.karelX < 4) {
    this.karelX += 1;
    }
    break;
    }
    }
    
    pressedAB() {
    this.isKarelActive = !this.isKarelActive;
    }
    }


### 关于作者

这个项目的作者是David Fisher博士（来自[罗斯-霍曼理工学院](https://www.rose-hulman.edu/academics/faculty/fisher-david-fisherds.html)的一位教授）。Fisher博士喜欢教育机器人，并且负责了很多户外编程活动，其中包括一次名为 [Connecting with Code](https://connectingwithcode.org/home)的夏令营。在这次夏令营中，他给每个参与者都分发了一块micro:bit。





