---
description: インタラクティブビデオビューアの設定属性。
solution: Experience Manager
title: VideoScrubber.timepattern
feature: Dynamic Media Classic，ビューア，SDK/API，インタラクティブビデオ
role: Developer,Business Practitioner
exl-id: d39ddf38-9157-412a-83a4-c1af4944a904
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---

# VideoScrubber.timepattern{#videoscrubber-timepattern}

インタラクティブビデオビューアの設定属性。

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 時間の吹き出しに表示する時間のパターンを設定します。<span class="codeph"> h</span>は時間を表し、<span class="codeph"> m</span>は分を表し、<span class="codeph"> s</span>は秒を表します。 </p> <p>各時間単位に使用される文字の数によって、その単位に表示する桁数が決まります。 指定した桁に収まらない数値は、後続の単位に表示されます。 </p> <p>例えば、現在のムービー時間が67分5秒の場合、<span class="codeph"> m:ss</span>は67:05と表示されます。 時間パターンが<span class="codeph"> h:mm:s</span>の場合は、同じ時間が1:07:5と表示されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`mm:s`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
timepattern=h:mm:ss
```
