---
title: VideoTime.timepattern
description: インタラクティブビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: de071adf-6c3c-4702-8950-8246b8ee459e
TQID: 'https://experienceleague.adobe.com/T2S4fAjAry5waLTPztxZjvDzVBVCoBqbfJXSZK-5SAQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 118
ht-degree: 2%

---

# VideoTime.timepattern{#videotime-timepattern}

インタラクティブビデオビューアの設定属性。

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> コントロールバーに表示される時間のパターンを設定します。ここで、<span class="codeph"> h</span>は時間、<span class="codeph"> m</span>は数分、<span class="codeph"> s</span>は数秒です。 </p> <p>時間単位ごとに使用される文字数によって、単位に表示する桁数が決まります。 数値が指定された数字に収まらない場合、同等の値が後続の単位に表示されます。 </p> <p>例えば、現在のムービー時間が67分5秒の場合、<span class="codeph"> m:ss</span>の時間パターンは67:05と表示されます。 時間パターンが<span class="codeph"> h:mm:s</span>の場合、同じ時間は1:07:5として表示されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

オプション。

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`m:ss`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
timepattern=h:mm:ss
```
