---
description: レイヤー画像
seo-description: レイヤー画像
seo-title: src
solution: Experience Manager
title: src
topic: Scene7 Image Serving - Image Rendering API
uuid: b4396848-b992-4371-a8ae-4ff1781ae1be
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# src{#src}

レイヤー画像

` src= *`objectnestedRequest`*|{[is|ir|fxg]'{' *``*'}'}`

<table id="simpletable_59104309B8284B21ABCE7DC95BF5A273"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> オブジェクト </span> </p> </td> 
  <td class="stentry"> <p>画像オブジェクト。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> nestedRequest </span> </p> </td> 
  <td class="stentry"> <p>ネストされた画像サービング、画像レンダリングまたは外部要求。 </p> </td> 
 </tr> 
</table>

## 説明 {#section-59ec6dc2afcb43efb34dbb0f7733543f}

イメージレイヤーのソースイメージを指定します。

*`object`* には、カタログエントリまたは画像/SVGファイルを指定できます。

objectを参 [照](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)。

入れ子のリクエストまたは埋め込みのリクエストは中括弧で囲まれます。 埋め込み画像サービング要求のプレフィッ `is`クスに、埋め込み画像レンダリング要求のプレフィ `ir`ックスに、FXGグラフィックレンダリング要求のプレフィックスを付けま `fxg`す。 プレフィックスが指定されていない場合、外部サーバーへの要求が想定されます。

リクエストの [ネストと埋め込みを参照してくださ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)い。

>[!NOTE]
>
>FXGグラフィックレンダリングは、Scene7のホスト環境でのみ使用でき、追加のライセンスが必要な場合があります。 詳しくは、Scene7サポートにお問い合わせください。

## プロパティ {#section-2c22bb89a35d470f833df8ba898efd93}

レイヤー属性。 ifに適 `layer=0` 用されま `layer=comp`す。 同じ層内で `text=` 互い `textPs=` に排他的で、、、またはの最後の値が使用さ `text=`れ、こ `textPs=`れが画 `src=` 像かテキストレイヤーかを判別します。 エフェクトレイヤーでは無視されます。

*`object`*またはコマンドを含む別のカタログレコードに解決さ `src=` れな `mask=` い可能性がありま `catalog::Modifier`す。 （同様の効果を得るには、リクエストのネストを使用します）。

、およ `is`びのプ `ir`リフィッ `fxg` クスでは大文字と小文字が区別されます。

## 初期設定 {#section-a92f3882041b4d43ae2caf014647165f}

レイヤー0の場合、URLのパスコンポーネントのオブジェクトが使用されます(指定しな `src=` い場合)。 他のレイヤーの初期設定値はありません。

## 関連項目 {#section-e467e03330564796932ac081f1c9c1d0}

[catalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f)text=textText= [mask](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)object, [mask](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)[object, Templates, Templates, Nesting Request, Embedding](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
