---
title: VideoTime.timepattern
description: Video360 ビューアの設定属性
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: a3a4f3f9-b6ef-4ee2-b006-578b743698ad
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 2%

---

# VideoTime.timepattern{#videotime-timepattern}

Video360 ビューアの設定属性

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> コントロールバーに表示される時間のパターンを設定します。<span class="codeph"> h</span> は時間、<span class="codeph"> m</span> は分、<span class="codeph"> s</span> は秒です。 </p> <p>時間単位ごとに使用される文字数によって、その単位に表示する桁数が決まります。 数値が指定の数字に収まらない場合は、対応する値が後続の単位で表示されます。 </p> <p>例えば、現在のムービーの時間が 67 分 5 秒の場合、タイムパターン <span class="codeph">m:ss</span> は 67:05 と表示されます。 指定した時間パターンが :07: h<span class="codeph">s:mm: の場合は、同じ時間が 1</span>5 と表示されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

オプション。

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`m:ss`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
timepattern=h:mm:ss
```
