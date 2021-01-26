---
description: ZoomView.transition
solution: Experience Manager
title: ZoomView.transition
topic: Dynamic Media
uuid: 1d58d230-f056-4cd8-a36f-b0f5d43483a3
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 4%

---


# ZoomView.transition{#zoomview-transition}

` [ZoomView.|<containerId>_zoomView.]transition= *``*[, *`timeeasing`*]`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 時間</span></span> </p> </td> 
   <td colname="col2"> <p> 1回のズームステップ操作に対するアニメーション処理にかかる時間を秒単位で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> easing</span></span> </p> </td> 
   <td colname="col2"> <p> 加速または減速の錯覚効果を作り出し、トランジションをより自然に表現します。 easingは、次のいずれかに設定できます。 </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0（自動） </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1（線形） </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2 (quadratic) </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3 (cubic) </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4 (quartic) </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5 (quintic) </li> 
     </ul> </p> <p>Autoモードでは、弾性ズームが無効の場合（初期設定）、常に線形トランジションが使用されます。 それ以外の場合は、トランジション時間に基づいて、他のいずれかのイージング関数に適合します。 つまり、トランジション時間が短いほど、加速または減速効果に高次のイージング関数が使用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`0.5,0`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`transition=2,2`
