---
description: 下位選択。 選択したオブジェクトまたはグループの異なる領域に異なるマテリアルを適用し、以前に適用したマテリアルを削除できます。
solution: Experience Manager
title: sub
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: c9968fbb-c38b-4180-81be-19992fa8f347
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 6%

---

# sub{#sub}

下位選択。 選択したオブジェクトまたはグループの異なる領域に異なるマテリアルを適用し、以前に適用したマテリアルを削除できます。

`sub=0|1|2|3|4|5`

<table id="simpletable_F6BF91BD2C4B47BF8A28032E392D37F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>壁全体を選択します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>壁の上半分を選択します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>壁の下半分を選択します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>上部の壁の境界領域を選択します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>中央の壁の境界領域を選択します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>下の壁境界領域を選択します。 </p> </td> 
 </tr> 
</table>

現在は、壁オブジェクトに対してのみサポートされています。 前のMSSを終了し、指定したサブ選択に適用するマテリアルの新しいMSSを開始します。

壁の残りの半分に別の材料が指定されていない限り、上壁または下壁に指定された材料が壁全体に適用されます。

## プロパティ {#section-b202139d6d0847cc8d520a154104ab9d}

選択コマンド；MSS区切り。

## 初期設定 {#section-5b45a167a17c451596e4c59b7d53c368}

`sub=0`

## 関連項目 {#section-1a993ee24f144d4fb8baef0cc431b53b}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)
