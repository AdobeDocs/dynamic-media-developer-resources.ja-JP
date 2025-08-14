---
title: VideoTime.timepattern
description: VideoTime.timepattern
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0c79b3e2-ac5a-43c3-ac52-8240e7ed3cc1
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 2%

---

# VideoTime.timepattern{#videotime-timepattern}

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_9FC55144166F406DB07DFE0C57791475"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> コントロールバーに表示される時間のパターンを設定します。<span class="codeph"> h</span> は時間、<span class="codeph"> m</span> は分、<span class="codeph"> s</span> は秒です。 </p> <p>時間単位ごとに使用される文字数によって、その単位に表示する桁数が決まります。 数値が指定の数字に収まらない場合は、対応する値が後続の単位で表示されます。 </p> <p>例えば、現在のムービーの時間が 67 分 5 秒の場合、タイムパターン <span class="codeph">m:ss</span> は 67:05 と表示されます。 指定した時間パターンが :07: h<span class="codeph">s:mm: の場合は、同じ時間が 1</span>5 と表示されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

オプション。

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`m:ss`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`timepattern=h:mm:ss`
