---
title: 整列
description: テクスチャレンダリングの整列。 選択したビネットオブジェクトで定義された原点のどれを使用するかを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b76f173-809b-4b41-bf39-6b85f77ab2db
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 整列 {#align}

テクスチャレンダリングの整列。 選択したビネットオブジェクトで定義された原点のどれを使用するかを指定します。

`align=0|1|2|3|4|5|6`

<table id="simpletable_D15233999E35488EB2F933BD72798E2F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>初期設定（中央一致）の原点です。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>連続一致の接触チャネル。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>ランダムな整列。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3.6 </p></td> 
  <td class="stentry"> <p>ユーザ定義の接触チャネル。 </p></td> 
 </tr> 
</table>

レンダラーは、テクスチャをオブジェクトに適用し、テクスチャのアンカーポイント ( `anchor=`) は、指定した原点と一致します。

各オブジェクトは、最大で 6 つの原点 (0、1、3、4、5、6) を定義できます。 次の場合、 `align` 値が指定されていますが、対応する原点がビネットオブジェクトによって定義されていません。既定の (center-match) 原点が使用されます。

`align=2` ランダムテクスチャの整列を指定します ( この場合、 `anchor=` は事実上無視されます。

ほとんどの場合、アパレル生地の場合は、隣接するオブジェクト間のテクスチャの整列を管理するために、表皮材に使用されます。

## プロパティ {#section-350fadc87dcf4812a8a02d1c3d6697a0}

材料属性。 壁、キャビネット、アプライアンス、窓のカバーフレームオブジェクトが選択されている場合、またはマテリアルが繰り返し可能なテクスチャでない場合は無視されます。

## 初期設定 {#section-3231c2854bae4477836b626ac208dd34}

`catalog::Alignment`マテリアルがカタログエントリに基づいている場合は、0 （中央一致）。

## 関連項目 {#section-945d1ce275df487d9d564d4043156c79}

[catalog::Alignment](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) , [anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
