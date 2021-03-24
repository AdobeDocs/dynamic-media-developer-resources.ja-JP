---
description: 画像マップデータ このレイヤーの画像マップデータを提供します。 この画層のカタログマップのデータを上書きします。
solution: Experience Manager
title: マップ
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 3%

---


# マップ{#map}

画像マップデータ このレイヤーの画像マップデータを提供します。 この画層のcatalog::Mapのデータを上書きします。

`map=[ *``*]mapA=[ *`stringstringA`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>このレイヤーの画像マップデータ（レイヤー座標）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> stringA</span></span> </p></td> 
  <td class="stentry"> <p>このレイヤーの画像マップデータ（ソース画像座標）。 </p></td> 
 </tr> 
</table>

空の文字列は、このレイヤーが画像マップを提供しないことを示します。 文字列は、解析上の問題を避けるために、適切にHTTPエンコードする必要があります。

*`string`*&#x200B;に含まれるすべてのアンパサンド(&amp;)文字は、HTTPエンコードする必要があります。

`mapA=`と`catalog::Map`はソース画像座標でマップデータを指定しますが、`map=`はレイヤー長方形の左上隅を基準とするレイヤー座標を（`rotate=`と`extend=`の後ろに）指定します。

出力画像マップは、常にレイヤーの長方形に合わせてクリップされます。 `shape`属性を省略した場合、または`default`に設定した場合、レイヤーの長方形全体が画像マップ領域として使用されます。

## プロパティ {#section-a18d9ea95c71414a905a68b8839c0843}

レイヤー属性。 `layer=comp`に適用すると、指定したマップデータが他のすべての画像マップの背後に重ね合わされます。 `req=map`以外は無視されます。 エフェクトレイヤーでは無視されます。 `mapA=` も指定し `map=` た場合は無視されます。

## 初期設定 {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` を指定し `map=` ない場合に使用されます。

## 例 {#section-cd7691c94f984222845c86dcb0051ce8}

単純なテキストレイヤー用の長方形の画像マップを定義します。

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

（ほとんどの場合）初期設定の属性を持つ`AREA`要素は、レイヤーの長方形全体のマップ領域を挿入するために使用されます。

## 関連項目 {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[画像マップ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)、 [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
