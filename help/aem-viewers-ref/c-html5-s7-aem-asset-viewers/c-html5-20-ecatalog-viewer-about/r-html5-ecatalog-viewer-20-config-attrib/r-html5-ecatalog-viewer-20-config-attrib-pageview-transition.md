---
description: PageView.transition
solution: Experience Manager
title: PageView.transition
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog
role: Developer,Business Practitioner
exl-id: aa12a210-88d9-4b96-b598-6967496ac668
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 4%

---

# PageView.transition{#pageview-transition}

` [PageView.|<containerId>_pageView.]transition= *``*[, *`timeeasing`*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 時間</span></span> </p> </td> 
   <td colname="col2"> <p> 1回のズームステップ操作でアニメーション処理にかかる時間を秒単位で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> easing</span></span> </p> </td> 
   <td colname="col2"> <p> 加速または減速の錯覚効果を作成し、トランジションをより自然に表現します。 easingは、次のいずれかに設定できます。 </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0 (auto) </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1 （線形） </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2 (quadratic) </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3 (cubic) </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4 (quartic) </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5 (quintic) </li> 
     </ul> </p> <p>Autoモードでは、弾性ズームが無効の場合（デフォルト）、常にリニアトランジションが使用されます。 それ以外の場合は、トランジション時間に基づいて、他のいずれかのイージング関数に適合されます。 つまり、トランジション時間が短いほど、イージング関数を使用して加速または減速効果が高くなります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-ebfd9162c8504666bf0e4485bf3b1383}

（オプション）

## 初期設定 {#section-9f91ce6567384ab691e4d4f8a7015455}

`0.5,0`

## 例 {#section-cb6b8793ee9946b8bf1cfddab8612db5}

`transition=2,2`
