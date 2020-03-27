---
description: テクスチャレンダリングの位置合わせ。 選択したビネットオブジェクトで定義された原点のどれを使用するかを指定します。
seo-description: テクスチャレンダリングの位置合わせ。 選択したビネットオブジェクトで定義された原点のどれを使用するかを指定します。
seo-title: align
solution: Experience Manager
title: align
topic: Scene7 Image Serving - Image Rendering API
uuid: 0b24cd82-f9b2-48f4-9052-8c2026370ff7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# align{#align}

テクスチャレンダリングの位置合わせ。 選択したビネットオブジェクトで定義された原点のどれを使用するかを指定します。

`align=0|1|2|3|4|5|6`

<table id="simpletable_D15233999E35488EB2F933BD72798E2F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>初期設定（中央一致）の原点。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>連続一致の原点。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>ランダムな配置。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3..6 </p></td> 
  <td class="stentry"> <p>ユーザー定義の原点。 </p></td> 
 </tr> 
</table>

レンダラーは、テクスチャのアンカーポイント( `anchor=`)が指定した原点に一致するように、テクスチャをオブジェクトに適用します。

各オブジェクトは、最大6つの原点(0,1, 3, 4, 5, 6)を定義できます。 値を指定し `align` たが、対応する原点がビネットオブジェクトで定義されていない場合は、初期設定の（中央一致）原点が使用されます。

`align=2` ランダムなテクスチャの整列を指定します。この場合、効果 `anchor=` 的に無視されます。

ほとんどの場合、アパレルファブリックなど、隣接するオブジェクト間のテクスチャの配置を管理するために、表皮材に使用されます。

## プロパティ {#section-350fadc87dcf4812a8a02d1c3d6697a0}

マテリアル属性。 壁、キャビネット、アプライアンス、窓のカバーフレームオブジェクトが選択されている場合、またはマテリアルが繰り返し可能なテクスチャでない場合は無視されます。

## 初期設定 {#section-3231c2854bae4477836b626ac208dd34}

`catalog::Alignment`に基づくマテリアルの場合は、カタログエントリに基づくマテリアル、それ以外の場合は0（中央揃え）。

## 関連項目 {#section-945d1ce275df487d9d564d4043156c79}

[catalog::Alignment](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) , [anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
