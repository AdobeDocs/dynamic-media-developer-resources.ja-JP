---
description: 画像マップデータ このレイヤのイメージマップデータを提供します。 この画層のカタログマップのデータを上書きします。
solution: Experience Manager
title: マップ
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 7c1fbb50-98ec-4d9a-b608-93d60d687069
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 3%

---

# マップ{#map}

画像マップデータ このレイヤのイメージマップデータを提供します。 この画層のcatalog::Mapのデータを上書きします。

`map=[ *``*]mapA=[ *`stringstringA`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 文字列</span></span> </p></td> 
  <td class="stentry"> <p>このレイヤーの画像マップデータ（レイヤー座標）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> stringA</span></span> </p></td> 
  <td class="stentry"> <p>このレイヤーの画像マップデータ（ソース画像座標）。 </p></td> 
 </tr> 
</table>

空の文字列は、このレイヤーが画像マップを提供しないことを示します。 文字列は、解析上の問題を避けるために、適切にHTTPエンコードする必要があります。

*`string`*&#x200B;に含まれるアンパサンド(&amp;)は、HTTPエンコードする必要があります。

`mapA=`と`catalog::Map`は、ソース画像座標でマップデータを指定しますが、`map=`は、（`rotate=`と`extend=`が適用された後の）レイヤー長方形の左上隅を基準として、レイヤー座標を指定します。

出力イメージマップは、常にレイヤーの長方形にクリップされます。 `shape`属性を省略した場合、または`default`に設定した場合は、画像マップ領域としてレイヤーの長方形全体が使用されます。

## プロパティ {#section-a18d9ea95c71414a905a68b8839c0843}

レイヤー属性。 `layer=comp`に適用すると、指定されたマップデータが他のすべての画像マップの後ろに重ね合わされます。 `req=map`以外は無視されます。 エフェクトレイヤでは無視されます。 `mapA=` も指定されてい `map=` る場合、は無視されます。

## 初期設定 {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` が指定されていない場 `map=` 合は、が使用されます。

## 例 {#section-cd7691c94f984222845c86dcb0051ce8}

単純なテキストレイヤーの長方形の画像マップを定義します。

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

（ほとんどの場合）初期設定の属性を持つ`AREA`要素を使用して、レイヤーの長方形全体のマップ領域を挿入します。

## 関連項目 {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[画像マップ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)、 [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
