---
title: ZoomView.transition
description: ZoomView.transition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: f1b4faa3-14d1-4eef-acc2-214c7be4a5ab
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 2%

---

# ZoomView.transition{#zoomview-transition}

` [ZoomView.|<containerId>_zoomView.]transition= *` 時間 `*[, *` 節約 `*]`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 時 </span></span> </p> </td> 
   <td colname="col2"> <p> 1 回のズームステップアクションでアニメーションが実行する時間を秒単位で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> ーシング </span></span> </p> </td> 
   <td colname="col2"> <p> 加速または減速の錯覚を作成します。これにより、トランジションがより自然に見えます。 イージングは、次のいずれかに設定できます。 </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0 （自動） </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1 （線形） </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2 （二次） </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3 （3 次） </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4 （クォート） </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5 （クインティック） </li> 
     </ul> </p> <p>自動モードでは、弾性ズームが無効な場合、常に直線遷移が使用されます（デフォルト）。 それ以外の場合は、遷移時間に基づいて他のイージング関数のいずれかに適合します。 すなわち、遷移時間が短いほど、イージング関数を高く使用して加減速効果を高める。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

オプション。

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`0.5,0`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`transition=2,2`
