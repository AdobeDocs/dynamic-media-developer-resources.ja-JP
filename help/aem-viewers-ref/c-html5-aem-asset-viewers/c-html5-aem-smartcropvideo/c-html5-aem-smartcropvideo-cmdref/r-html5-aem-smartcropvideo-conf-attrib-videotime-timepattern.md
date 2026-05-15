---
title: VideoTime.timepattern
description: スマート切り抜きビデオビューアの設定属性。
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: b63818e2-8da0-4965-b7d6-5ecd7ab5cdca
TQID: 'https://experienceleague.adobe.com/Cm3pgVjX5bs7SgZKgniuSxLD4AcEGgO8Iu6MNugZOvA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 2%

---

# VideoTime.timepattern{#videotime-timepattern}

スマート切り抜きビデオビューアの設定属性。

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> コントロールバーに表示される時間のパターンを設定します。<span class="codeph"> h</span>は時間、<span class="codeph"> m</span>は分、<span class="codeph"> s</span>は秒です。 </p> <p>時間単位ごとに使用される文字数によって、単位に表示する桁数が決まります。 数値が指定された数字に収まらない場合、同等の値が後続の単位に表示されます。 </p> <p>例えば、現在のムービー時間が67分5秒の場合、時間パターン <span class="codeph"> m:ss</span>は67:05として表示されます。 指定された時間パターンが<span class="codeph"> h:mm:s</span>の場合、同じ時間は1:07:5として表示されます。 </p> </td> 
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
