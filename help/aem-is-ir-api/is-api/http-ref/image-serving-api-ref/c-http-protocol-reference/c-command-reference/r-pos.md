---
title: pos
description: レイヤーの位置：
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2e9a1f3-7216-4ab0-9c37-57f083119cef
TQID: 'https://experienceleague.adobe.com/9UMGN0TeM4mZ0IZI--dEA3KBYKOVhJxCJMZuPevlq8o'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 169
ht-degree: 2%

---

# pos{#pos}

レイヤーの位置：

pos= *`coord`*

posN= *`coordN`*

<table id="simpletable_754F76EE00BF4129B07502647FF172B7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> コード </span> </p> </td> 
  <td class="stentry"> <p>このレイヤーの原点からレイヤー0の原点（int、int）までのピクセルオフセット。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>このレイヤーの原点からレイヤー0の原点までの正規化されたオフセット（実数、実数）。 </p></td> 
 </tr> 
</table>

画像、テキストおよび単色レイヤーがある場合、`pos=`は、レイヤー0 アンカーに対するレイヤーアンカーの位置を指定します。 `posN=`座標の値は、実際のレイヤー0の直角サイズに対して正規化されます。

エフェクトレイヤーがある場合、`pos=`は親レイヤーに対してエフェクトレイヤーを移動します。

正の値を指定すると、レイヤーは右/下に、負の値は左/上に移動します。 `posN=0.5,0.5`では、レイヤーをレイヤー0の幅と高さの半分だけ下および右に移動します。

## プロパティ {#section-51a60cdc52d040538fef378ace7c2e7d}

レイヤー属性。 `layer=0`または`layer=comp`の場合、無視されます。

## 初期設定 {#section-70a6bc71ded5494e843194dfb6bf5a6c}

`posN=0,0`. この座標は、画像、テキスト、または単色レイヤーの場合、レイヤー0 アンカーと同じ位置にレイヤーアンカーを配置します。 エフェクトレイヤーを親レイヤーの上または下に直接配置します。

## 例 {#section-a89a02c22f6b4260bfcf7c842cd6069d}

[ テンプレート ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)の例Aを参照してください。

## 関連項目 {#section-812d95575ba542808e8387d0a8650606}

[origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)
