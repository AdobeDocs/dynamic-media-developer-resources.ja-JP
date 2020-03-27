---
description: レイヤーの位置
seo-description: レイヤーの位置
seo-title: pos
solution: Experience Manager
title: pos
topic: Scene7 Image Serving - Image Rendering API
uuid: e9872ce9-5c47-49c5-9c87-4fa8441c4770
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# pos{#pos}

レイヤーの位置

pos= *`coord`*

posN= *`coordN`*

<table id="simpletable_754F76EE00BF4129B07502647FF172B7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> コード</span> </p> </td> 
  <td class="stentry"> <p>このレイヤーの原点からレイヤー0の原点（整数、整数）へのピクセルオフセット。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>このレイヤーの原点からレイヤー0の原点（実数、実数）への正規化されたオフセット。 </p></td> 
 </tr> 
</table>

画像、テキストおよびべた塗りのレイヤーの場合、レイヤー0 `pos=` のアンカーを基準とするレイヤーアンカーの位置を指定します。 `posN=` 座標値は、実際のレイヤーの0矩形サイズを基準に正規化されます。

エフェクトレイヤーの場合は、親レ `pos=` イヤーを基準にしてエフェクトレイヤーを移動します。

正の値を指定すると、レイヤーは右/下に向かって移動し、負の値を指定すると左/上に向かって移動します。 `posN=0.5,0.5` レイヤーを0の幅と高さの半分だけ下および右に移動します。

## プロパティ {#section-51a60cdc52d040538fef378ace7c2e7d}

レイヤー属性。 またはの場合は無 `layer=0` 視されま `layer=comp`す。

## 初期設定 {#section-70a6bc71ded5494e843194dfb6bf5a6c}

`posN=0,0`. これにより、レイヤーアンカーが画像、テキストまたはべた塗りのレイヤーの場合、レイヤー0アンカーと同じ場所に配置されます。 エフェクトレイヤーを親レイヤーの上または下に配置します。

## 例 {#section-a89a02c22f6b4260bfcf7c842cd6069d}

テンプレートの例Aを参照し [てくださ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)い。

## 関連項目 {#section-812d95575ba542808e8387d0a8650606}

[origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)
