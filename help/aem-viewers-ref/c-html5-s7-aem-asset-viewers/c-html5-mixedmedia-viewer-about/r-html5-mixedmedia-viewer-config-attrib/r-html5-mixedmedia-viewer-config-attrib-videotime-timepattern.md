---
description: VideoTime.timepattern
solution: Experience Manager
title: VideoTime.timepattern
feature: Dynamic Media Classic，ビューア，SDK/API，混在メディアセット
role: Developer,Business Practitioner
exl-id: 0c79b3e2-ac5a-43c3-ac52-8240e7ed3cc1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 3%

---

# VideoTime.timepattern{#videotime-timepattern}

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_9FC55144166F406DB07DFE0C57791475"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> コントロールバーに表示する時間のパターンを設定します。<span class="codeph"> h</span>は時間、<span class="codeph"> m</span>は分、<span class="codeph"> s</span>は秒を表します。 </p> <p>各時間単位に使用される文字の数によって、その単位に表示する桁数が決まります。 指定した桁に収まらない数値は、後続の単位に表示されます。 </p> <p>例えば、現在のムービー時間が67分5秒の場合、時間パターン<span class="codeph"> m:ss</span>は67:05と表示されます。 所定の時間パターンが<span class="codeph"> h:mm:s</span>の場合、同じ時間が1:07:5と表示されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`m:ss`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`timepattern=h:mm:ss`
