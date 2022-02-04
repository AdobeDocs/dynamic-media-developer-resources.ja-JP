---
title: VideoScrubber.timepattern
description: ビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: e0956a0b-4d82-475f-8990-8b059014233a
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 3%

---

# VideoScrubber.timepattern{#videoscrubber-timepattern}

ビデオビューアの設定属性。

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 時間の吹き出しに表示する時間のパターンを設定します。ここで、 <span class="codeph"> h</span> 時間 <span class="codeph"> m</span> は分、 <span class="codeph"> s</span> は秒です。 </p> <p>各時間単位に使用される文字の数によって、その単位で表示する桁数が決まります。 指定された桁数に収まらない場合は、対応する値が後続の単位で表示されます。 </p> <p>例えば、現在のムービーの時間が 67 分 5 秒の場合、時間のパターン <span class="codeph"> m:ss</span> は 67:05 と表示されます。 同じ時刻が 1 と表示されます:07:指定された時間パターンが <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

（オプション）

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`m:ss`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
timepattern=h:mm:ss
```
