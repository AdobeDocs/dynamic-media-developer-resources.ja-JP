---
title: PageView.transition
description: PageView.transition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: aa12a210-88d9-4b96-b598-6967496ac668
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 2%

---

# PageView.transition{#pageview-transition}

` [PageView.|<containerId>_pageView.]transition= *` 時間 `*[, *` 節約 `*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 時 </span></span> </p> </td> 
   <td colname="col2"> <p> 1 回のズームステップアクションでアニメーションが実行する時間を秒単位で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> ーシング </span></span> </p> </td> 
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

## プロパティ {#section-ebfd9162c8504666bf0e4485bf3b1383}

オプション。

## 初期設定 {#section-9f91ce6567384ab691e4d4f8a7015455}

`0.5,0`

## 例 {#section-cb6b8793ee9946b8bf1cfddab8612db5}

`transition=2,2`
