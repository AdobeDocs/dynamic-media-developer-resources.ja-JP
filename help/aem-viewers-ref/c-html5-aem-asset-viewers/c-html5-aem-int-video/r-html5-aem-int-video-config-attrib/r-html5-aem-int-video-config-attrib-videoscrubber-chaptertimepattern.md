---
title: VideoScrubber.chaptertimepattern
description: インタラクティブビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 93c1d38c-1f45-4794-8084-f520f9caf257
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 3%

---

# VideoScrubber.chaptertimepattern{#videoscrubber-chaptertimepattern}

インタラクティブビデオビューアの設定属性。

`[VideoScrubber.|<containerId>_videoScrubber.]chaptertimepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> チャプターラベルのタイトルバーに表示する時間のパターンを設定します。<span class="codeph"> h</span>は時間を表し、<span class="codeph"> m</span>は分を表し、<span class="codeph"> s</span>は秒を表します。 </p> <p>各時間単位に使用される文字の数によって、その単位に表示する桁数が決まります。 指定した桁に収まらない数値は、後続の単位に表示されます。 </p> <p>例えば、現在のムービー時間が67分5秒の場合、<span class="codeph"> m:ss</span>は67:05と表示されます。 時間パターンが<span class="codeph"> h:mm:s</span>の場合は、同じ時間が1:07:5と表示されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`m:ss`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
chaptertimepattern=h:mm:ss
```
