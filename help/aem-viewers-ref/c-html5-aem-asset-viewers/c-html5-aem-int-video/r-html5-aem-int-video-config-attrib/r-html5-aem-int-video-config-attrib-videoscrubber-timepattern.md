---
title: VideoScrubber.timepattern
description: インタラクティブビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: d39ddf38-9157-412a-83a4-c1af4944a904
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 2%

---

# VideoScrubber.timepattern{#videoscrubber-timepattern}

インタラクティブビデオビューアの設定属性。

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> タイムバブルに表示される時間のパターンを設定します。<span class="codeph"> h</span> は時間を、<span class="codeph"> m</span> は分を、<span class="codeph"> s</span> は秒を表します。 </p> <p>時間単位ごとに使用される文字数によって、その単位に表示する桁数が決まります。 数値が指定の数字に収まらない場合は、対応する値が後続の単位で表示されます。 </p> <p>例えば、現在のムービーの時間が 67 分 5 秒の場合、<span class="codeph"> m:ss</span> のタイムパターンは 67:05 と表示されます。 時間パターンが :07: h<span class="codeph">s:mm: の場合は、同じ時間が 1</span>5 と表示されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

オプション。

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`mm:s`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
timepattern=h:mm:ss
```
