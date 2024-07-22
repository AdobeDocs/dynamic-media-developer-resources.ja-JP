---
title: src
description: レイヤー画像。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 88b89e70-59cf-4fb9-bbe7-0ac5eff792f1
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 2%

---

# src{#src}

レイヤー画像。

` src= *`object`*|{[is|ir|fxg]'{' *`nestedRequest`*'}'}`

<table id="simpletable_59104309B8284B21ABCE7DC95BF5A273"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> object </span> </p> </td> 
  <td class="stentry"> <p>画像オブジェクト。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> nestedRequest </span> </p> </td> 
  <td class="stentry"> <p>ネストされた画像サービング、画像レンダリングまたは外部リクエスト。 </p> </td> 
 </tr> 
</table>

## 説明 {#section-59ec6dc2afcb43efb34dbb0f7733543f}

画像レイヤーのソース画像を指定します。

カタログエントリまたは画像/SVGファイルのい *`object`* れかです。

[object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) を参照してください。

ネストされたリクエストまたは埋め込まれたリクエストは、中括弧で囲まれます。 埋め込み画像サービングリクエストの前に `is`、埋め込み画像レンダリングリクエストの前に `ir`、FXG グラフィックレンダリングリクエストの前に `fxg` を付けます。 プレフィックスが指定されていない場合、外部サーバーへのリクエストが想定されます。

[ ネストおよび埋め込みのリクエスト ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b) を参照してください。

## プロパティ {#section-2c22bb89a35d470f833df8ba898efd93}

レイヤー属性。 `layer=comp` の場合は `layer=0` に適用されます。 同じレイヤー内で `text=` と `textPs=` を相互に排他的です。`text=`、`textPs=`、`src=` のいずれかの最後のオカレンスが優先され、これが画像レイヤーかテキストレイヤーかを判断します。 エフェクトレイヤーで無視されます。

*`object`*は、`catalog::Modifier` に `src=` または `mask=` コマンドを含む別のカタログレコードに解決されない場合があります。 （同様の効果を得るにはリクエストのネストを使用します）。

`is`、`ir`、`fxg` の各プレフィックスでは大文字と小文字が区別されます。

## 初期設定 {#section-a92f3882041b4d43ae2caf014647165f}

レイヤー 0 の場合、URL のパスコンポーネントのオブジェクトが使用されます（`src=` が指定されていない場合）。 他のレイヤーのデフォルト値はありません。

## 関連項目 {#section-e467e03330564796932ac081f1c9c1d0}

[catalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md)、[attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)、[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f)、[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)、[mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)、[object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)、[Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)、[ リクエストのネストと埋め込み ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
