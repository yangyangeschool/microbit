# Micro:bit -- 螢火蟲同步閃

[最後成果](https://youtu.be/V71hu5AyOkw)

[讓你的 micro:bit 搖身一變成螢火蟲](https://makecode.microbit.org/projects/fireflies)

## How do fireflies synchronize?

從 http://ncase.me/fireflies/ 閱讀關於螢火蟲同步發光的奧秘。

### 摘要：


1. 每一隻螢火蟲都有一個內在的時鐘，當時鐘「跑到12時」，螢火蟲就閃一下。
2. 當你（螢火蟲）看見鄰居閃一下時，`nudge`（輕推）一下時鐘，就是把時鐘稍微往前調快一點。
3. 完成

### 用 micro:bit 實作

先讓螢火蟲閃一下：
![](https://i.imgur.com/46Mj9Pz.png)

`每一隻螢火蟲都有一個內在的時鐘`，新增一個變數叫做 `clock`
![](https://i.imgur.com/mnH9SgM.png)

`當時鐘「跑到12時」，螢火蟲就閃一下`：
![](https://i.imgur.com/exQx6H9.png)

`當你（螢火蟲）看見鄰居閃一下時，`nudge`（輕推）一下時鐘，就是把時鐘稍微往前調快一點`。在 micro:bit 上需要：閃的時候廣播一個訊號；另一方面，收到訊號的人調快自己的時鐘：


閃的時候廣播一個訊號
![](https://i.imgur.com/ubW9XeM.png)

收到訊號的人調快自己的時鐘
![](https://i.imgur.com/xJYXKWp.png)

設定群組及訊號強弱
![](https://i.imgur.com/LaLBRBM.png)

全部程式：
![](https://i.imgur.com/E0uzC2H.png)

https://makecode.microbit.org/_KK6fum6ayKFg

## 其它

https://youtu.be/2rquixg7KqM

https://youtu.be/mw9rPniHngI
