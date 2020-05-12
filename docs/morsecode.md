# Micro:bit -- 摩斯電碼

[toc]

<!--
- [Micro Morse Phone](https://make.techwillsaveus.com/microbit/activities/micro-morse-phone)
- [Morse Code on the BBC micro:bit!](https://medium.com/groklearning/morse-code-on-the-bbc-micro-bit-1ea7eaad8f2)
- [Morse Code Transmitter](https://tinkercademy.com/tutorials/microbit-morse-code-transmit-receive/)
- [A Morse Code Transceiver On a Microbit](https://github.com/jg00dman/m0rvj_microbit_cw_transceiver)
-->

## 編碼

>王大同現在10歲，而他的同學正好住在他家對面，他的房間正好隔著一條小路就在王大同
房間的正對面。王大同和他的同學三更半夜不想睡，想聊天，但是沒有電話，沒有手機，
當然也沒有網路，他們怎麼辦？
這時，王大同的腦海閃過：「就是那個光」。為了躲在棉被裡看書，王大同昨天買了一隻
手電筒，剛好，他對面的同學也買了一隻。於是隔天王大同很開心的告訴他的同學，這樣
那樣、那樣這樣。當天晚上他們就用手電筒聊起來了。

你可以想像他們是怎麼用手電筒聊天的嗎？

- 用手電筒比劃出字母的形狀
- 用手電筒一閃一閃的方式：A閃1次；B閃2次；C閃3次…Z閃26次
- 中文也可以-用手電筒比劃出注音符號的形狀

上面的用法，可能說了一次「我要去 zoo」就不用了。不過你已經離解決問題愈來愈近了。如果你上網查一下，就會發現很早以前就有神奇的「**摩斯電碼**」了。於是你可以研究一下摩斯電碼，重新和你的同學學習如何「寫」字、如何「讀」字！

編碼或代碼(code)通常指一種在人和機器之間進行訊息轉換的系統。換句話說，編碼就是交流。有時候，我們誤以為編碼是「密碼」，其實大多數的編碼並不是這樣的。人們在相互溝通時，使用了各種不同的編碼，因為使用場合的不同，某些編碼方式比其它的更便利。只要一種編碼可以適用於其它編碼所不能適用的場合，它就是有用的編碼。計算機中使用了各種不同的編碼來傳遞和存儲數字、聲音、音樂、圖片和視訊…。這也就是為什麼老師一再強調在認識電腦時，編碼是很重要的概念。摩斯電碼和計算機也許沒有太大的相關，但是熟悉它的本質，對同學深入了解計算機會有很大的幫助！

- 口語、語音：我們用嘴巴發出聲音，讓聽得到的人，了解我們所用的語言的人聽懂
- 書面語言、文字：寫在紙上，如書信、報紙、雜誌
- 手語、點字

## 什麼是摩斯電碼

![](https://i.imgur.com/gEP8JMr.png)

這是一張摩斯電碼表。有兩種「符號」用來表示字元：點（.）和劃（-），或叫「滴」（Dit）和「答」（Dah）。點的長度決定了發報的速度，並且被當作發報時間參考。下面是時間控制的圖示：

```
-- --- .-. ... .    /    -.-. --- -.. .
M   O   R   S  E  (空格)  C    O   D  E
```

劃一般是三個點的長度；點劃之間的間隔是一個點的長度；字元之間的間隔是三個點的長度；單詞之間的間隔是七個點的長度。初學者往往被教導發送點劃間隔短小、短而快的字元，並且在符號和單詞之間誇大間隔時間。比較起來，這種方式更加容易學會。熟悉摩斯碼的人之間經常像這樣說話或拼寫（其中，「長音 / Dah」是發「awe」的音）：

```
 --     ---       .-.      ...    .   /    -.-.        ---      -..   .
DahDah DahDahDah DiDahDit DiDiDit Dit , DahDiDahDit DahDahDah DahDiDi Di
```

再簡單述說摩斯電碼的組成：


- 短音為基本單位，短音記為 DOT，唸作 DIH 或”滴”（ㄉㄧ˙輕聲）。
- 長音為 3 個短音的長度，長音記為 DASH，唸作 “DAH” 或”答”(ㄉㄚ)。
- 同一個字元中，短音與長音間的間隔為 1 個短音的長度。
- 字元與字元間的間隔為3個短音的長度。
- 字組 (WORD) 與字組間的間隔為 5～7 個短音的長度。

如果你想練習，有兩個網站很不錯：

- [learn morse code](http://www.learnmorsecode.com/)
- [Morse Code Translator](https://morsecode.world/international/translator.html)

就讓我們練習一下，用 morse code 「寫」字吧！

## 摩斯電碼解碼

要發送摩斯電碼很容易，只要去查一下(字母->摩斯電碼)編碼表就好了；但是接收時就不是那麼簡單了。這樣的一張表對我們了解摩斯電碼是如何構成的並沒有太大的幫助。如果你是那個接收且要「解碼」的人，你要怎麼辦呢？忘記那些字母順序吧！
忘記那些字母順序吧！

對，就是<span style="font-size:2em; color: red;">忘記那些字母順序吧！</span>，讓我們重新分析一下這個表，可以如何用另一種「角度」來建構它。

首先，我們發現，摩斯電碼表中每個字母的長度不一定一樣長，我們不如就反過來，從編碼後的長度來分析。

1 個「點」或「劃」：
![](https://i.imgur.com/zUNsLme.png)

2 個「點」或「劃」：
![](https://i.imgur.com/TjUmpVV.png)

3 個「點」或「劃」：
![](https://i.imgur.com/3XRuEKI.png)

4 個「點」或「劃」：
![](https://i.imgur.com/oe5ri1m.png)

在分析的過程中，你是不是發現，和以前在學2進制時一樣？沒有錯，是一樣的，而且它在不同點劃數所可以做的編碼數和2進制是一樣的：

|點劃數 | 可編碼數 | 可編碼數       | 可編碼數   |
|------| -------| ------------- |-----------|
| 1    | 2      | 2             | 2         |
| 2    | 4      | $2 \times 2$  | $2^2$     |
| 3    | 8      | $2 \times 2 \times 2$      | $2^3$     |
| 4    | 16     | $2 \times 2 \times 2 \times 2$  | $2^4$     |


你會發現，我們還可以將上面的分析表畫成下面這樣的一張「二元分歧樹」的圖。如果你認真想一想，會發現事先建立這樣的一張表是定義摩斯電碼所必需的。首先，它保證不會犯給不同的字母相同的編碼值的錯誤！其次，它保證你使用了全部的可用碼，而且「點」與「劃」的編碼沒有多餘的位數！當然，這張圖在我們要「解碼」時，非常地好用。
![](https://i.imgur.com/7wWsWRI.png)

摩斯電碼被稱為二元碼(binary code)，因為編碼中僅含有兩種狀態：點與劃。二元事物、二元編碼常常用2的冪次方來描述，在電腦科學中更是常被用到。上面對二元編碼所做的分析在數學上叫做組合學或組合分析，而這個也只是一個非常簡單的練習。從這些練習中，同學們應該對「編碼」<->「解碼」有更進一步的體認。

# 使用 micro:bit 實作

## 在 micro:bit 使用廣播實作

首先，我們做一個 di 函數
![](https://i.imgur.com/1VqlLdq.png)

再做一個 da 函數
![](https://i.imgur.com/8wy9o7E.png)

通訊的時候，因為是雙向可同時溝通，所以做一個 over
![](https://i.imgur.com/ADtsoAj.png)

按鍵規畫：按 A 是 di；按 B 是 da；按 AB 是 over
![](https://i.imgur.com/QASHF2v.png)

廣播
![](https://i.imgur.com/w0yrT49.png)

廣播前要設定群組
![](https://i.imgur.com/qTuGnOe.png)

收廣播訊號
![](https://i.imgur.com/AAwSHrN.png)

全部程式
![](https://i.imgur.com/3DDrXsS.png)

https://makecode.microbit.org/_3kfR5UVdW1gW

## 在 micro:bit 使用金手指實作

