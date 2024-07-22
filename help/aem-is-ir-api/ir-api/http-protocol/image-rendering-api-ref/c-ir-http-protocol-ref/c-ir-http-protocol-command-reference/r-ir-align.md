---
title: align
description: テクスチャ レンダリングの位置合わせ。 選択したビネット オブジェクトによって定義された原点のうちどれを使用するかを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b76f173-809b-4b41-bf39-6b85f77ab2db
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 3%

---

# align {#align}

テクスチャ レンダリングの位置合わせ。 選択したビネット オブジェクトによって定義された原点のうちどれを使用するかを指定します。

`align=0|1|2|3|4|5|6`

<table id="simpletable_D15233999E35488EB2F933BD72798E2F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>既定値（中央一致）の原点。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>連続一致原点。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>ランダムな配置。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3..6 </p></td> 
  <td class="stentry"> <p>ユーザー定義オリジン。 </p></td> 
 </tr> 
</table>

レンダラは、テクスチャのアンカーポイント（`anchor=`）が指定された原点に一致するように、オブジェクトにテクスチャを適用します。

各オブジェクトは、最大 6 つの原点（0、1、3、4、5、6）を定義できます。 `align` の値が指定されていても、対応する原点がビネット オブジェクトによって定義されていない場合は、既定（center-match）の原点が使用されます。

`align=2` ランダムなテクスチャの位置合わせを指定します。この場合、`anchor=` は無視されます。

ほとんどの場合、隣接するオブジェクト間のテクスチャの配置を管理するために、室内装飾品の材料、おそらくアパレル生地に使用されます。

## プロパティ {#section-350fadc87dcf4812a8a02d1c3d6697a0}

マテリアル アトリビュート。 壁、キャビネット、アプライアンス、または窓の覆いのフレーム オブジェクトが選択されている場合、またはマテリアルが繰り返し可能なテクスチャでない場合は無視されます。

## 初期設定 {#section-3231c2854bae4477836b626ac208dd34}

マテリアルがカタログ エントリに基づいている場合は `catalog::Alignment`、それ以外の場合は 0 （中央一致）。

## 関連項目 {#section-945d1ce275df487d9d564d4043156c79}

[catalog::Alignment](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) , [anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
