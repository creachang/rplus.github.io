---
layout: post
category : Demo
title: 以PNG透明度及底色模擬css sprite
tagline: 減少圖片大小
tags : [demo, css, F2E, css sprite, InkScape]
---
{% include JB/setup %}
###[CSS Sprite](https://www.google.com.tw/search?q=CSS+Sprite):
這個效果其實個人還蠻喜歡用的  
除了減少 request 次數，讓網頁似乎可以載入快些外  
若沒做此項圖片處理的網頁在滑鼠 hover 過去時，會造成圖片切間的閃爍

    > 因為此時的背景圖已切換到 `:hover{bg-img:url(~~~);}` 的規則了
    > 但裡頭的圖剛正在載入ing，所以底圖會暫時是空的，也就造成了視覺上的閃爍

css sprite因為將 hover 前後的圖放在一塊，  
在 hover 時以 `background-position` 來做狀態的切換  
也就不會有圖片的閃爍狀況了

css sprite 的缺點大概就是圖都兜在了一起  
牽一髮而動全身  
要做修改時會比較麻煩~  
一開始做位置定位時也較花時間  
但網路也有不少 sprite 的產生器，將這動作懶人化了~  
相當棒~

不過其實想說的並不是css sprite  
(只是拿來塞文字 充板面XD)

雖然 css sprite 相當好用  
但有時候其實多觀察一下要用的圖  
可以發現很多圖示類的圖片可以有另外一種的作法(我不敢打包票是比較好的作法XD)  
利用透明度以及半透前景與背景的色彩混色  
將能以一張圖示，來達到不同狀態的切換

這樣的作法只需要一張圖就可以了  
而或許也可讓圖示顏色的自由度高一些  
(藉由改變背景色 來製造一些不同顏色的圖示)  
但其實說實在的，這種半透明圖片處理實在比較麻煩就是了 orz  
而且初始就要想一堆這圖片要怎麼弄怎麼調的，實在也是搞肛啦~  
不過以實驗來說，是還蠻好玩的啦XDD

<iframe src="http://rplus.github.com/Demo/heart/heart.html" width="100%" height="350"> </iframe>

###Demo Link:
<http://rplus.github.com/Demo/heart/heart.html>