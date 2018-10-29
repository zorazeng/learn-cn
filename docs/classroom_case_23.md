## 感染

这里蔓延着一种疾病。你能找到patient zero（疾病源）吗？

感染是一款已经发布的游戏。这款游戏主要是模仿疾病的传播。游戏的目标是在每个玩家死亡之前组织疾病蔓延。
- 玩家的数量：1个主玩家和4个从玩家，或者更多其他玩家。所有玩家都需要使用一块micro:bit和电池组。

在这个游戏中，主玩家的micro:bit感染了一种疾病，也就是首个玩家(“patient zero”)携带了疾病。被感染的玩家是立刻被感染的，但是在孵化期却不会有任何的发病迹象。疾病的传染是发生在两块micro:bit足够靠近的时候。过了孵化期之后，屏幕上会显示一个哭脸。过了发病期，玩家最终将会死亡，并且屏幕上会显示一个头骨。死亡的玩家就出局了。

如果至少有一个玩家在感染中活下来了，游戏获胜。否则，重新再玩一次吧！

感染是一个参与性的游戏，它要求学生们四处走动。我们建议在户外或者在一个开阔的区域玩这个游戏，给这个活动更多的空间。

### 如何玩

按下按钮`A+B`进入到主玩家模式（这个游戏只有一个主要玩家）。
等待玩家来配对。已配对玩家的数量将会显示在屏幕上。一旦配对成功，玩家的屏幕上会显示一个字母，这个字母就是玩家的身份。
一旦所有的玩家都配对成功，按下按钮`A+B`来启动感染游戏。这个游戏会随机选择一个玩家作为**patient zero**（疾病源）。

如果靠的足够近（检测到一个较强的`RSSI`信号)，或者满足了一种疾病传播的可能性(`TRANSMISSIONPROB`)，一个玩家就会把疾病传染给另一个玩家。在孵化期(`INCUBATION`)中，玩家不会显示任何的发病迹象（笑脸）。在孵化期过后，玩家开始发病，并在屏幕上显示一个哭脸。在哭脸显示后，玩家死亡并显示一个头骨。

当游戏结束，micro:bit将会显示玩家的ID(身份)（`A`, `B`, `C`…)、健康程度以及感染者的身份。主玩家的micro:bit将会显示patient zero（疾病源）的身份。

游戏中用到的图标：

- 配对中：IconNames.Ghost
- 已配对：IconNames.Happy
- 死亡：IconNames.Skull
- 生病：IconNames.Sad
- 孵化中：IconNames.Confused
- 健康：IconNames.Happy

### 项目分享

这个程序使用的语言特征（例如：`switch`或`enum`）在blocks（积木块）中不支持。因此，它不能被转换为blocks（积木块）。

[https://makecode.microbit.org/_gymCJCWPbiDu](https://makecode.microbit.org/_gymCJCWPbiDu)

### JavaScript代码


    /**
     * Infection game
     * 
     * Flash all micro:bit will this script
     * 
     * Press A+B to enter master mode (1 per game)
     *
     * Wait for players to be paired. The number of paired player will display on screen.
     * An icon will appear on player's screen.
     * 
     * Press A+B to start the infection game. The master will pick a random
     * player as patient zero.
     *
     * A player will transmit the disease if close enough (RSSI)
     * and with a certain probability (TRANSMISSIONPROB). 
     * During the incudation phase (INCUBATION), the player does not show any sign 
     * of illness. After that phase, the sad face shows up.
     * 
     * The game will automatically stop once all players are dead or healthy. The master can
     * also press A+B again to stop the game.
     * 
     * Once the game is over, the micro:bit will show the player id (A,B,C...), health and 
     * who infected him.
     * 
     * Icons used in the game:
     * 
     * Pairing: IconNames.Ghost
     * Paired: IconNames.Happy
     * Dead: IconNames.Skull
     * Sick: IconNames.Sad
     * Incubating: IconNames.Confused
     * Healthy: IconNames.Happy
     * 
     */
    const INCUBATION = 20000; // time before showing symptoms
    const DEATH = 40000; // time before dying off the disease
    const RSSI = -45; // db
    const TRANSMISSIONPROB = 40; // % probability to transfer disease
    
    enum GameState {
    Stopped,
    Pairing,
    Running,
    Over
    }
    
    enum HealthState {
    Healthy,
    Incubating,
    Sick,
    Dead
    }
    
    const GameIcons = {
    Pairing: IconNames.Ghost,
    Paired: IconNames.Happy,
    Dead: IconNames.Skull,
    Sick: IconNames.Sad,
    Incubating: IconNames.Confused,
    Healthy: IconNames.Happy
    }
    
    const playerIcons = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
    class Player {
    id: number;
    icon: number;
    health: HealthState;
    show() {
    basic.showString(playerIcons[this.icon]);
    }
    }
    
    // common state
    let state = GameState.Stopped;
    
    // master state
    let master = false;
    let patientZero: Player;
    const players: Player[] = [];
    
    // player state
    let paired = false;
    let infectedBy = -1; // who infected (playerIcon)
    let infectedTime = 0; // local time when infection happened
    let playerIcon = -1; // player icon and identity
    let health = HealthState.Healthy;
    
    // get a player instance (creates one as needed)
    function player(id: number): Player {
    for (const p of players)
    if (p.id == id) return p;
    
    // add player to game
    let p = new Player();
    p.id = id;
    p.icon = (players.length + 1) % playerIcons.length;
    p.health = HealthState.Healthy;
    players.push(p);
    serial.writeLine(`player ==> ${p.id}`)
    
    return p;
    }
    
    function allDead(): boolean {
    for (const p of players)
    if (p.health != HealthState.Dead) return false;
    return true;
    }
    
    function gameOver() {
    state = GameState.Over;
    if (patientZero)
    patientZero.show();
    }
    
    function gameFace() {
    switch (state) {
    case GameState.Stopped:
    basic.showIcon(GameIcons.Pairing);
    break;
    case GameState.Pairing:
    if (playerIcon > -1)
    basic.showString(playerIcons[playerIcon]);
    else
    basic.showIcon(paired ? GameIcons.Paired : GameIcons.Pairing, 1);
    break;
    case GameState.Running:
    switch (health) {
    case HealthState.Dead:
    basic.showIcon(GameIcons.Dead, 1);
    break;
    case HealthState.Sick:
    basic.showIcon(GameIcons.Sick, 1);
    break;
    default:
    basic.showIcon(GameIcons.Healthy, 1);
    break;
    }
    break;
    case GameState.Over:
    // show id
    basic.showString(playerIcons[playerIcon]);
    basic.pause(2000);
    // show health
    switch (health) {
    case HealthState.Dead:
    basic.showIcon(GameIcons.Dead, 2000);
    break;
    case HealthState.Sick:
    basic.showIcon(GameIcons.Sick, 2000);
    break;
    case HealthState.Incubating:
    basic.showIcon(GameIcons.Incubating, 2000);
    break;
    default:
    basic.showIcon(GameIcons.Healthy, 2000);
    break;
    }
    // show how infected
    if (infectedBy > -1) {
    basic.showString(" INFECTED BY");
    basic.showString(playerIcons[infectedBy]);
    basic.pause(2000);
    } else {
    basic.showString(" PATIENT ZERO");
    basic.pause(2000);
    }
    // show score
    game.showScore();
    basic.pause(1000);
    break;
    }
    }
    
    // master button controller
    input.onButtonPressed(Button.AB, () => {
    // register as master
    if (state == GameState.Stopped && !master) {
    master = true;
    paired = true;
    state = GameState.Pairing;
    serial.writeLine("registered as master");
    radio.setTransmitPower(7); // beef up master signal
    basic.showString("0");
    return;
    }
    
    if (!master) return; // master only beyond this
    
    // launch game
    if (state == GameState.Pairing) {
    // pick 1 player and infect him
    patientZero = players[Math.random(players.length)];
    while (patientZero.health == HealthState.Healthy) {
    radio.sendValue("infect", patientZero.id);
    basic.pause(100);
    }
    
    // all ready
    state = GameState.Running;
    serial.writeLine(`game started ${players.length} players`);
    
    // show startup
    basic.showIcon(GameIcons.Dead);
    } // end game 
    else if (state == GameState.Running) {
    gameOver();
    }
    })
    
    radio.setGroup(42);
    radio.setTransmitSerialNumber(true)
    radio.onDataPacketReceived(({ time, receivedNumber, receivedString, signal, serial: id }) => {
    if (master) {
    if (receivedString == "pair") {
    // register player
    let n = players.length;
    let p = player(id);
    // show player number if changed
    if (n != players.length) {
    led.stopAnimation();
    basic.showNumber(players.length);
    }
    }
    else if (receivedString == "health") {
    let p = player(id);
    p.health = receivedNumber;
    // check if all infected
    if (allDead())
    gameOver();
    }
    } else {
    if (receivedString == "state") {
    // update game state
    state = receivedNumber as GameState;
    } else if (infectedBy < 0 &&
    receivedString == "infect"
    && receivedNumber == control.deviceSerialNumber()) {
    // infected by master
    infectedBy = 0; // infected my master
    infectedTime = input.runningTime();
    health = HealthState.Incubating;
    serial.writeLine(`infected ${control.deviceSerialNumber()}`);
    }
    if (receivedString == "h" + control.deviceSerialNumber().toString() &&
    health < receivedNumber) {
    health = receivedNumber;
    }
    switch (state) {
    case GameState.Pairing:
    // medium range in pairing mode
    if (!paired &&
    receivedString == "paired"
    && receivedNumber == control.deviceSerialNumber()) {
    // paired!
    serial.writeLine(`player paired ==> ${control.deviceSerialNumber()}`)
    paired = true;
    return;
    }
    else if (paired && receivedString == "i" + control.deviceSerialNumber().toString()) {
    playerIcon = receivedNumber;
    }
    break;
    case GameState.Running:
    // broadcast infection status
    if (health == HealthState.Healthy && receivedString == "transmit") {
    serial.writeLine(`signal: ${signal}`);
    if (signal > RSSI &&
    Math.random(100) > TRANSMISSIONPROB) {
    infectedBy = receivedNumber;
    infectedTime = input.runningTime();
    health = HealthState.Incubating;
    }
    } else if (health != HealthState.Dead
    && receivedString == "health" && signal > RSSI) {
    game.addScore(1);
    }
    break;
    }
    }
    })
    
    // main game loop
    basic.forever(() => {
    if (master) {
    switch (state) {
    case GameState.Pairing:
    // tell each player they are registered
    for (const p of players) {
    radio.sendValue("paired", p.id);
    radio.sendValue("i" + p.id, p.icon);
    }
    serial.writeLine(`pairing ${players.length} players`);
    basic.pause(500);
    break;
    case GameState.Running:
    for (const p of players) {
    radio.sendValue("h" + p.id, p.health);
    }
    break;
    case GameState.Over:
    if (patientZero)
    patientZero.show();
    break;
    }
    radio.sendValue("state", state); // keep broadcasting the game state
    } else { // player loop
    switch (state) {
    case GameState.Pairing:
    // broadcast player id
    if (playerIcon < 0)
    radio.sendValue("pair", control.deviceSerialNumber());
    else if (infectedBy > -1)
    radio.sendValue("health", health);
    break;
    case GameState.Running:
    // update health status
    if (health != HealthState.Healthy && input.runningTime() - infectedTime > DEATH)
    health = HealthState.Dead;
    else if (health != HealthState.Healthy && input.runningTime() - infectedTime > INCUBATION)
    health = HealthState.Sick;
    // transmit disease
    if (health == HealthState.Incubating || health == HealthState.Sick)
    radio.sendValue("transmit", playerIcon);
    radio.sendValue("health", health);
    break;
    }
    // show current animation
    gameFace();
    }
    })
    
    basic.showIcon(GameIcons.Pairing)







<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_6rtRwyfYs2Ed" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>

