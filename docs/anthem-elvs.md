# 校歌

[二林工商校歌](https://makecode.microbit.org/_3epY3Whvf8e3)

音階--頻率對照表

![](https://i.imgur.com/ZLpIhlm.png)

二林工商校歌歌譜

![](https://i.imgur.com/aUXEPAy.png)

以 500ms 為一拍

```javascript
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index <= tone.length - 1; index++) {
        music.playTone(tone[index], beat[index])
    }
})
let beat: number[] = []
let tone: number[] = []
tone = [784, 880, 659, 587, 523, 784, 784, 659, 784, 880, 1, 1046, 1175, 880, 1046, 784, 659, 880, 784, 659, 587, 1, 659, 784, 659, 880, 784, 1175, 1046, 880, 1046, 784, 1, 1046, 659, 880, 784, 659, 880, 1046, 659, 587, 523, 1, 1046, 784, 1046, 659, 784, 784, 784, 659, 880, 1, 1046, 1175, 880, 1046, 659, 880, 784, 587, 1, 659, 587, 523, 659, 784, 880, 784, 659, 1046, 880, 1, 784, 659, 784, 880, 1175, 659, 1318, 1175, 1046, 1046, 1]
beat = [500, 500, 250, 250, 500, 375, 125, 250, 250, 500, 500, 500, 500, 250, 250, 500, 375, 125, 250, 250, 500, 500, 500, 250, 250, 500, 500, 375, 125, 250, 250, 500, 500, 500, 250, 250, 500, 500, 375, 125, 250, 250, 500, 500, 500, 500, 500, 500, 375, 125, 250, 250, 500, 500, 500, 500, 500, 500, 250, 500, 250, 500, 500, 500, 250, 250, 500, 500, 250, 250, 375, 125, 500, 500, 500, 375, 125, 500, 500, 250, 250, 375, 125, 500, 500]
basic.forever(function () {
	
})
```
