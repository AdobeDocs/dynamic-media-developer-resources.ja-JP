---
description: レイヤー画像。
seo-description: レイヤー画像。
seo-title: src
solution: Experience Manager
title: src
topic: Dynamic Media Image Serving - Image Rendering API
uuid: b4396848-b992-4371-a8ae-4ff1781ae1be
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 3%

---


# src{#src}

レイヤー画像。

` src= *`objectnestedRequest`*|{[is|ir|fxg]'{' *``*'}'}`

<table id="simpletable_59104309B8284B21ABCE7DC95BF5A273"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> オブジェクト </span> </p> </td> 
  <td class="stentry"> <p>画像オブジェクト。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> nestedRequest  </span> </p> </td> 
  <td class="stentry"> <p>ネストされた画像サービング、画像レンダリングまたは外部要求。 </p> </td> 
 </tr> 
</table>

## 説明 {#section-59ec6dc2afcb43efb34dbb0f7733543f}

イメージレイヤーのソースイメージを指定します。

*`object`* は、カタログエントリまたは画像/SVGファイルのいずれかです。

[オブジェクト](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)を参照してください。

入れ子のリクエストや埋め込みのリクエストは、中括弧で囲みます。 埋め込まれた画像サービング要求の先頭に`is`、埋め込まれた画像レンダリング要求の先頭に`ir`を、FXGグラフィックレンダリング要求の先頭に`fxg`を付けます。 プレフィックスが指定されていない場合、外部サーバーへの要求と見なされます。

「[リクエストのネストと埋め込み](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)」を参照してください。

## プロパティ {#section-2c22bb89a35d470f833df8ba898efd93}

レイヤー属性。 `layer=comp`の場合は`layer=0`に適用されます。 同じ層の`text=`と`textPs=`とは相互に排他的です。`text=`、`textPs=`、または`src=`の最後の値が使用され、これが画像かテキストレイヤーかが判断されます。 エフェクトレイヤーでは無視されます。

*`object`*`catalog::Modifier`内に`src=`または`mask=`コマンドを含む別のカタログレコードに解決できない場合があります。 （同様の効果を得るには、リクエストのネストを使用します）。

`is`、`ir`、`fxg`のプリフィックスでは大文字と小文字が区別されます。

## 初期設定 {#section-a92f3882041b4d43ae2caf014647165f}

レイヤー0の場合、`src=`が指定されていない場合、URLのパスコンポーネントのオブジェクトが使用されます。 他のレイヤーの初期設定値はありません。

## 関連項目 {#section-e467e03330564796932ac081f1c9c1d0}

[catalog::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ,  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), text=textText= [, mask, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f)mask,  [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) [mask, object=, Path Templates, Templates, Nesting Request Embedding](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
