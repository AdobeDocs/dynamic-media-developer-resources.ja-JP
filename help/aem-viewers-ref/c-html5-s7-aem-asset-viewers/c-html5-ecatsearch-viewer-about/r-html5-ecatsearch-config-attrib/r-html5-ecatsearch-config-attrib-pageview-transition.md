---
description: PageView.transition
solution: Experience Manager
title: PageView.transition
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e9db5c83-e6cf-4847-99b3-a1cf6a1fbe9f
TQID: 'https://experienceleague.adobe.com/pZVulT-xLqHZZqr0Ma00DjQBMrvzpyIrZr8RFZmXSXA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 107
ht-degree: 2%

---

# PageView.transition{#pageview-transition}

[!DNL `[PageView.|<containerId>_pageView.]transition= *`時間`*[, *` イージング `*]`]

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">時間</span></span> </p> </td> 
   <td colname="col2"> <p> 1つのズームステップアクションのアニメーションにかかる時間を秒単位で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> イージング </span></span> </p> </td> 
   <td colname="col2"> <p> 加速または減速の錯覚を作成し、トランジションをより自然に見せます。 イージングは、次のいずれかに設定できます。 </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0 （自動） </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1 （リニア） </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2 （2次） </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3 （立方） </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4 （四分位数） </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5 （クインティック） </li> 
     </ul> </p> <p>自動モードでは、弾性ズームが無効になっている場合は常に線形遷移が使用されます（デフォルト）。 それ以外の場合は、移行時間に基づいて他のイージング関数の1つに適合します。 すなわち、遷移時間が短いほど、緩和関数が加速度または減速効果を加速するために使用される。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-ebfd9162c8504666bf0e4485bf3b1383}

オプション。

## 初期設定 {#section-9f91ce6567384ab691e4d4f8a7015455}

[!DNL `0.5,0`]

## 例 {#section-cb6b8793ee9946b8bf1cfddab8612db5}

[!DNL `transition=2,2`]
