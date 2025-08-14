---
title: マップ
description: 画像マップデータ。 このレイヤーの画像マップデータを提供します。 この画層のカタログ マップのデータを上書きします。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7c1fbb50-98ec-4d9a-b608-93d60d687069
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 2%

---

# マップ{#map}

画像マップデータ。 このレイヤーの画像マップデータを提供します。 この画層の catalog::Map のデータを上書きします。

`map=[ *`string`*]mapA=[ *`stringA`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 文字列 </span></span> </p></td> 
  <td class="stentry"> <p>この画層のイメージ マップ データを画層の座標で表示します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> stringA</span></span> </p></td> 
  <td class="stentry"> <p>ソース画像座標でのこのレイヤーの画像マップデータ。 </p></td> 
 </tr> 
</table>

空の文字列は、このレイヤーが画像マップを提供してはならないことを示します。 解析の問題を回避するには、文字列を適切に HTTP エンコードする必要があります。

*`string`* で使用されるアンパサンド（&amp;）文字は、すべて http エンコードする必要があります。

`mapA=` と `catalog::Map` はソース イメージ座標でマップ データを指定しますが、`map=` はレイヤの長方形の左上のコーナーを基準にしたレイヤ座標を想定します（`rotate=` と `extend=` が適用された後）。

出力画像マップは、常にレイヤーの長方形にクリップされます。 `shape` 属性を省略するか `default` に設定すると、レイヤーの長方形全体が画像マップ領域として使用されます。

## プロパティ {#section-a18d9ea95c71414a905a68b8839c0843}

レイヤー属性。 `layer=comp` に適用すると、指定されたマップ データは、他のすべてのイメージ マップの背後にレイヤ化されます。 `req=map` でない限り無視されます。 エフェクトレイヤーで無視されます。 `mapA=` も指定されている場合、`map=` は無視されます。

## 初期設定 {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` は、`map=` が指定されていない場合に使用されます。

## 例 {#section-cd7691c94f984222845c86dcb0051ce8}

単純なテキストレイヤー用に長方形の画像マップを定義します。

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

レイヤーの長方形全体のマップ領域を挿入するには、（ほとんど）デフォルトの属性を持つ `AREA` 要素を使用します。

## 関連項目 {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[ 画像マップ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab), [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
