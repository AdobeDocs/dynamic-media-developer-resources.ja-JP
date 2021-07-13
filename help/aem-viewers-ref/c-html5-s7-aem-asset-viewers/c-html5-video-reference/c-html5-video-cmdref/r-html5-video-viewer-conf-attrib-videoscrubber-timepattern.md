---
description: ビデオビューアの設定属性。
solution: Experience Manager
title: VideoScrubber.timepattern
feature: Dynamic Media Classic，ビューア，SDK/API，ビデオ
role: Developer,User
exl-id: e0956a0b-4d82-475f-8990-8b059014233a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---

# VideoScrubber.timepattern{#videoscrubber-timepattern}

ビデオビューアの設定属性。

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 時間バブルに表示する時間のパターンを設定します。<span class="codeph"> h</span>は時間、<span class="codeph"> m</span>は分、<span class="codeph"> s</span>は秒を表します。 </p> <p>各時間単位に使用される文字の数によって、その単位に表示する桁数が決まります。 指定した桁に収まらない数値は、後続の単位に表示されます。 </p> <p>例えば、現在のムービー時間が67分5秒の場合、時間パターン<span class="codeph"> m:ss</span>は67:05と表示されます。 所定の時間パターンが<span class="codeph"> h:mm:s</span>の場合、同じ時間が1:07:5と表示されます。 </p> </td> 
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
