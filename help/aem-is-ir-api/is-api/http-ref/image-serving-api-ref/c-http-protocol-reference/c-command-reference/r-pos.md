---
title: 位置
description: レイヤーの位置。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2e9a1f3-7216-4ab0-9c37-57f083119cef
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 2%

---

# 位置{#pos}

レイヤーの位置。

pos= *`coord`*

posN= *`coordN`*

<table id="simpletable_754F76EE00BF4129B07502647FF172B7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>このレイヤーの原点からレイヤーの原点までのピクセルオフセット（int、int）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>このレイヤの原点からレイヤ 0 の原点（実際、実際）への正規化されたオフセット。 </p></td> 
 </tr> 
</table>

画像、テキスト、および単色のレイヤーがある場合は、レイヤー 0 アンカー `pos=` 対するレイヤーアンカーの位置を指定します。 `posN=` 座標の値は、実際のレイヤ 0 の長方形サイズを基準に正規化されます。

エフェクトレイヤーが存在する場合、`pos=` は親レイヤーを基準にしてエフェクトレイヤーを移動します。

正の値を指定すると、レイヤーは右/下に移動し、負の値を指定すると左/上に移動します。 ま `posN=0.5,0.5`、レイヤーの幅と高さがレイヤーの半分の幅と高さで上下に移動します。

## プロパティ {#section-51a60cdc52d040538fef378ace7c2e7d}

レイヤー属性。 `layer=0` または `layer=comp` の場合、無視されます。

## 初期設定 {#section-70a6bc71ded5494e843194dfb6bf5a6c}

`posN=0,0`。 この座標は、画像、テキスト、または単色のレイヤーの場合、レイヤーアンカーをレイヤー 0 アンカーと同じ場所に配置します。 エフェクトレイヤーを親レイヤーの上または下に直接配置します。

## 例 {#section-a89a02c22f6b4260bfcf7c842cd6069d}

[&#x200B; テンプレート &#x200B;](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) の例 A を参照してください。

## 関連項目 {#section-812d95575ba542808e8387d0a8650606}

[接触チャネル =](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)
