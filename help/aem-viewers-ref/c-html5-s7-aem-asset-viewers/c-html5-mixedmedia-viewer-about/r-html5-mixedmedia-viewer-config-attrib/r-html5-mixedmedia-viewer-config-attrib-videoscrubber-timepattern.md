---
description: VideoScrubber.timepattern
solution: Experience Manager
title: VideoScrubber.timepattern
topic: Dynamic media
uuid: 6034dc22-c1d4-4a37-93de-42a88b99234a
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 3%

---


# VideoScrubber.timepattern{#videoscrubber-timepattern}

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_D1D7BE09311B469983B52E34338FEAFE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 時間の吹き出しに表示する時間のパターンを設定します。<span class="codeph"> h</span>は時間、<span class="codeph"> m</span>は分、<span class="codeph"> s</span>は秒を表します。 </p> <p>各時間単位に使用される文字数によって、その単位に表示する桁数が決まります。 指定した桁数に収まらない場合は、後続の単位に相当する値が表示されます。 </p> <p>例えば、現在のムービー時間が67分5秒の場合、時間パターン<span class="codeph"> m:ss</span>は67:05と表示されます。 指定した時間パターンが<span class="codeph"> h:mm:s</span>の場合、同じ時間が1:07:5と表示されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`m:ss`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`timepattern=h:mm:ss`
