---
description: レイヤーの位置
solution: Experience Manager
title: pos
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: c2e9a1f3-7216-4ab0-9c37-57f083119cef
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 3%

---

# pos{#pos}

レイヤーの位置

pos= *`coord`*

posN= *`coordN`*

<table id="simpletable_754F76EE00BF4129B07502647FF172B7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> コード</span> </p> </td> 
  <td class="stentry"> <p>このレイヤーの原点からレイヤー0の原点（整数、整数）までのピクセルオフセット。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>このレイヤの原点からレイヤ0の原点（実数、実数）への正規化オフセット。 </p></td> 
 </tr> 
</table>

画像、テキスト、ソリッドカラーレイヤーの場合、 `pos=`は、レイヤー0アンカーを基準としたレイヤーアンカーの位置を指定します。 `posN=` 座標値は、実際のレイヤ0の直角サイズに対して正規化されます。

エフェクトレイヤーの場合、`pos=`は、エフェクトレイヤーを親レイヤーに対して相対的にシフトします。

正の値を指定すると、レイヤーは右/下に向かって移動し、負の値を指定すると左/上に向かって移動します。 `posN=0.5,0.5` レイヤーを0の幅と高さの半分だけ下および右に移動します。

## プロパティ {#section-51a60cdc52d040538fef378ace7c2e7d}

レイヤー属性。 `layer=0`または`layer=comp`の場合は無視されます。

## 初期設定 {#section-70a6bc71ded5494e843194dfb6bf5a6c}

`posN=0,0`. これが画像、テキスト、またはべた塗りのカラーのレイヤーの場合、レイヤーアンカーはレイヤー0アンカーと同じ場所に配置されます。 エフェクトレイヤーを親レイヤーの上または下に配置します。

## 例 {#section-a89a02c22f6b4260bfcf7c842cd6069d}

[テンプレート](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)の例Aを参照してください。

## 関連項目 {#section-812d95575ba542808e8387d0a8650606}

[origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)
