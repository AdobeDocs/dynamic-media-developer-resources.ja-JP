---
description: 'null'
seo-description: 'null'
seo-title: SpinView.transition
solution: Experience Manager
title: SpinView.transition
topic: Dynamic media
uuid: d5cc319a-fb0b-41d3-a118-f00376a127e4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 4%

---


# SpinView.transition{#spinview-transition}

` [SpinView.|<containerId>_spinView.]transition= *``*[, *`timeeasing`*]`

<table id="table_5B8094216AE94DC59671E06DB941A366"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 時間</span></span> </p> </td> 
   <td colname="col2"> <p> 1回のズームステップ操作に対するアニメーション処理にかかる時間を秒単位で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> easing</span></span> </p> </td> 
   <td colname="col2"> <p> 加速または減速の錯覚効果を作り出し、トランジションをより自然に表現します。 easingは、次のいずれかに設定できます。 </p> <p> 
     <ul id="ul_7B9694978D96449AB986AED1CF7F649D"> 
      <li id="li_904CEC8AD5834139A5585EE70ACE9C80">0（自動） </li> 
      <li id="li_471D4CD39C10415497B1714B0AD961B9"> 1（線形） </li> 
      <li id="li_7A0F9F1186604E75BAA19626A844236A"> 2 (quadratic) </li> 
      <li id="li_B8D4C40D795642AB835925582B707158"> 3 (cubic) </li> 
      <li id="li_2B9F7324BB89455C89C1CAE1BD5BBB65"> 4 (quartic) </li> 
      <li id="li_B94A553B6E844247BE88ECA0A8CEB811"> 5 (quintic) </li> 
     </ul> </p> <p>Autoモードでは、弾性ズームが無効の場合（初期設定）、常に線形トランジションが使用されます。 それ以外の場合は、トランジション時間に基づいて、他のいずれかのイージング関数に適合します。 つまり、トランジション時間が短いほど、加速または減速効果に高次のイージング関数が使用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0.5,0`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=2,2`
