---
description: 下位選択。 選択したオブジェクトまたはグループの異なる領域に異なるマテリアルを適用したり、以前に適用したマテリアルを削除したりできます。
seo-description: 下位選択。 選択したオブジェクトまたはグループの異なる領域に異なるマテリアルを適用したり、以前に適用したマテリアルを削除したりできます。
seo-title: sub
solution: Experience Manager
title: sub
topic: Scene7 Image Serving - Image Rendering API
uuid: cb9f4dc5-9d89-483a-ae72-b9076b27c57e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 6%

---


# sub{#sub}

下位選択。 選択したオブジェクトまたはグループの異なる領域に異なるマテリアルを適用したり、以前に適用したマテリアルを削除したりできます。

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
  <td class="stentry"> <p>下の壁の境界領域を選択します。 </p> </td> 
 </tr> 
</table>

現在、壁オブジェクトに対してのみサポートされています。 前のMSSを終了し、指定したサブ開始に適用するマテリアルの新しいMSSを選択します。

壁の残りの半分に別のマテリアルを指定しない限り、上または下の壁に指定したマテリアルが壁全体に適用されます。

## プロパティ {#section-b202139d6d0847cc8d520a154104ab9d}

選択コマンド；MSS区切り文字。

## 初期設定 {#section-5b45a167a17c451596e4c59b7d53c368}

`sub=0`

## 関連項目 {#section-1a993ee24f144d4fb8baef0cc431b53b}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)
