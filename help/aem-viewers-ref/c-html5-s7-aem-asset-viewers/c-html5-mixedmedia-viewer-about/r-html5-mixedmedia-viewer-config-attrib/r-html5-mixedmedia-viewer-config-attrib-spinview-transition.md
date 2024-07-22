---
title: SpinView.transition
description: SpinView.transition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: fcffe282-65a5-4093-8838-71a64085b387
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 2%

---

# SpinView.transition{#spinview-transition}

` [SpinView.|<containerId>_spinView.]transition= *` 時間 `*[, *` 節約 `*]`

<table id="table_5B8094216AE94DC59671E06DB941A366"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 時 </span></span> </p> </td> 
   <td colname="col2"> <p> 1 回のズームステップアクションでアニメーションが実行する時間を秒単位で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> ーシング </span></span> </p> </td> 
   <td colname="col2"> <p> 加速または減速の錯覚を作成します。これにより、トランジションがより自然に見えます。 イージングは、次のいずれかに設定できます。 </p> <p> 
     <ul id="ul_7B9694978D96449AB986AED1CF7F649D"> 
      <li id="li_904CEC8AD5834139A5585EE70ACE9C80">0 （自動） </li> 
      <li id="li_471D4CD39C10415497B1714B0AD961B9"> 1 （線形） </li> 
      <li id="li_7A0F9F1186604E75BAA19626A844236A"> 2 （二次） </li> 
      <li id="li_B8D4C40D795642AB835925582B707158"> 3 （3 次） </li> 
      <li id="li_2B9F7324BB89455C89C1CAE1BD5BBB65"> 4 （クォート） </li> 
      <li id="li_B94A553B6E844247BE88ECA0A8CEB811"> 5 （クインティック） </li> 
     </ul> </p> <p>自動モードでは、弾性ズームが無効な場合、常に直線遷移が使用されます（デフォルト）。 それ以外の場合は、遷移時間に基づいて他のイージング関数のいずれかに適合します。 すなわち、遷移時間が短いほど、イージング関数を高く使用して加減速効果を高める。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

オプション。

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0.5,0`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=2,2`
