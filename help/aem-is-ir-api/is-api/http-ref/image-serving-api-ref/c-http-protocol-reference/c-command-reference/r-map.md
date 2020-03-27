---
description: 画像マップデータ このレイヤーの画像マップデータを提供します。 この画層のカタログマップのデータを上書きします。
seo-description: 画像マップデータ このレイヤーの画像マップデータを提供します。 この画層のカタログマップのデータを上書きします。
seo-title: マップ
solution: Experience Manager
title: マップ
topic: Scene7 Image Serving - Image Rendering API
uuid: 9c1c3323-21ab-4820-bf4e-761b82ada1ab
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# マップ{#map}

画像マップデータ このレイヤーの画像マップデータを提供します。 この画層のcatalog::Mapのデータを上書きします。

`map=[ *``*]mapA=[ *`stringstringA`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 文字列</span></span> </p></td> 
  <td class="stentry"> <p>このレイヤーの画像マップデータ（レイヤー座標）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> string <span class="varname"> A</span></span> </p></td> 
  <td class="stentry"> <p>このレイヤーの画像マップデータ（ソース画像座標）。 </p></td> 
 </tr> 
</table>

空の文字列は、このレイヤーが画像マップを提供しないことを示します。 文字列は、解析上の問題を避けるために、適切にHTTPエンコードする必要があります。

で使用されるアンパサンド(&amp;)文字は、すべてHTTPエ *`string`* ンコードする必要があります。

マップ `mapA=` データ `catalog::Map` をソース画像座標で指定する際、では、レイヤーの長方形の左上隅と `map=` 左隅を基準にして、レイヤーの座標を(後で適用した後 `rotate=` で) `extend=` 指定します。

出力画像マップは、常にレイヤーの長方形に合わせてクリップされます。 属性を省略し `shape` た場合、またはに設定した場 `default`合、レイヤーの長方形全体が画像マップ領域として使用されます。

## プロパティ {#section-a18d9ea95c71414a905a68b8839c0843}

レイヤー属性。 に適用すると、指定し `layer=comp`たマップデータが他のすべての画像マップの背後に重ね合わされます。 次の場合を除いて無視さ `req=map`れます。 エフェクトレイヤーでは無視されます。 `mapA=` も指定されて `map=` いる場合は無視されます。

## 初期設定 {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` が指定されていない場 `map=` 合に使用されます。

## 例 {#section-cd7691c94f984222845c86dcb0051ce8}

単純なテキストレイヤー用の長方形の画像マップを定義します。

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

(ほとんど `AREA` が)初期設定の属性を持つ要素は、レイヤーの長方形全体のマップ領域を挿入するために使用されます。

## 関連項目 {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[画像マップ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)、 [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
