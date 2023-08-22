---
title: マップ
description: 画像マップデータ。 このレイヤの画像マップデータを提供します。 この画層のカタログマップのデータを上書きします。
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

画像マップデータ。 このレイヤの画像マップデータを提供します。 この画層の catalog::Map のデータを上書きします。

`map=[ *`文字列`*]mapA=[ *`stringA`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 文字列</span></span> </p></td> 
  <td class="stentry"> <p>このレイヤーの画像マップデータ（レイヤー座標）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> stringA</span></span> </p></td> 
  <td class="stentry"> <p>このレイヤーの画像マップデータ（ソース画像の座標）。 </p></td> 
 </tr> 
</table>

空の文字列は、このレイヤーが画像マップを提供しないことを示します。 解析上の問題を回避するために、文字列は適切に HTTP エンコードする必要があります。

アンパサンド (&amp;) 文字が *`string`* は http エンコードする必要があります。

While `mapA=` および `catalog::Map` ソースイメージ座標でマップデータを指定します。 `map=` レイヤーの長方形の左上隅を基準として、レイヤーの座標を指定します ( `rotate=` および `extend=` が適用されている場合 )。

出力イメージマップは、常にレイヤーの長方形にクリップされます。 次の場合、 `shape` 属性が省略されたか、 `default`を指定した場合、画層の長方形全体が画像マップ領域として使用されます。

## プロパティ {#section-a18d9ea95c71414a905a68b8839c0843}

レイヤー属性。 適用先： `layer=comp`を指定した場合、指定したマップデータが他のすべての画像マップの背後にレイヤー化されます。 次の場合を除き無視 `req=map`. 効果画層で無視されます。 `mapA=` 次の場合は無視されます： `map=` も指定されます。

## 初期設定 {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` 次の場合に使用されます。 `map=` が指定されていません。

## 例 {#section-cd7691c94f984222845c86dcb0051ce8}

単純なテキストレイヤーの長方形の画像マップを定義します。

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

An `AREA` （ほとんど）デフォルトの属性を持つ要素は、レイヤーの長方形全体のマップ領域を挿入するために使用されます。

## 関連項目 {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[画像マップ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab), [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
