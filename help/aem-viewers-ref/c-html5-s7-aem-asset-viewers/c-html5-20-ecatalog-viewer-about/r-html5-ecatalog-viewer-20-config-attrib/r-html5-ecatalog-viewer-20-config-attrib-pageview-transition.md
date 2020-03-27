---
description: 'null'
seo-description: 'null'
seo-title: PageView.transition
solution: Experience Manager
title: PageView.transition
topic: Dynamic media
uuid: f84da456-ac02-4037-b1fd-7440823eb1ef
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PageView.transition{#pageview-transition}

` [PageView.|<containerId>_pageView.]transition= *`時`*[, *`間`*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 時間</span></span> </p> </td> 
   <td colname="col2"> <p> 1回のズームステップ操作のアニメーションにかかる時間を秒単位で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> easing</span></span> </p> </td> 
   <td colname="col2"> <p> 加速または減速の錯覚効果を作成し、トランジションがより自然に表示されるようにします。 easingは、次のいずれかに設定できます。 </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0（自動） </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1（線形） </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2(quadratic) </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3 (cubic) </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4（4等分） </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5 (quintic) </li> 
     </ul> </p> <p>Autoモードでは、弾性ズームが無効の場合（初期設定）、常に線形トランジションが使用されます。 それ以外の場合は、トランジション時間に基づいて、他のいずれかのイージング関数に適合します。 つまり、トランジション時間が短いほど、加速または減速効果を加速するためにイージング関数が高くなります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-ebfd9162c8504666bf0e4485bf3b1383}

（オプション）

## 初期設定 {#section-9f91ce6567384ab691e4d4f8a7015455}

`0.5,0`

## 例 {#section-cb6b8793ee9946b8bf1cfddab8612db5}

`transition=2,2`
