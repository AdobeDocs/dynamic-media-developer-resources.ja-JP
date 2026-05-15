---
title: src
description: レイヤー画像：
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 88b89e70-59cf-4fb9-bbe7-0ac5eff792f1
TQID: 'https://experienceleague.adobe.com/4BChH5cLIy-7A3mnQqqo0S7Z4XfoC4T-34gI-YM-tGY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 192
ht-degree: 2%

---

# src{#src}

レイヤー画像：

` src= *` オブジェクト `*|{[is|ir|fxg]'{' *`nestedRequest`*'}'}`

<table id="simpletable_59104309B8284B21ABCE7DC95BF5A273"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> オブジェクト </span> </p> </td> 
  <td class="stentry"> <p>画像オブジェクト： </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> nestedRequest </span> </p> </td> 
  <td class="stentry"> <p>ネストされた画像サービング、画像レンダリング、または外部リクエスト。 </p> </td> 
 </tr> 
</table>

## 説明 {#section-59ec6dc2afcb43efb34dbb0f7733543f}

画像レイヤーのソース画像を指定します。

*`object`*&#x200B;は、カタログ項目または画像/SVG ファイルのいずれかである可能性があります。

[&#x200B; オブジェクト &#x200B;](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)を参照してください。

ネストされたリクエストまたは埋め込まれたリクエストは、中括弧で囲まれます。 埋め込み画像サービングリクエストの先頭に`is`、埋め込み画像レンダリングリクエストに`ir`、FXG グラフィックレンダリングリクエストに`fxg`を付けます。 接頭辞が指定されていない場合、外部サーバーへのリクエストが想定されます。

[&#x200B; ネストと埋め込みのリクエスト &#x200B;](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)を参照してください。

## プロパティ {#section-2c22bb89a35d470f833df8ba898efd93}

レイヤー属性。 `layer=comp`の場合は`layer=0`に適用されます。 同じレイヤー内の`text=`と`textPs=`は相互に排他的です。最後に`text=`、`textPs=`、または`src=`が優先され、これが画像レイヤーかテキストレイヤーかを判断します。 エフェクトレイヤーでは無視されます。

*`object`*は、`src=`または`mask=` コマンドを`catalog::Modifier`に含む別のカタログ レコードに解決できません。 （リクエストネストを使用して、同様の効果を実現します）。

`is`、`ir`および`fxg`の接頭辞では、大文字と小文字が区別されます。

## 初期設定 {#section-a92f3882041b4d43ae2caf014647165f}

レイヤー0の場合、`src=`が指定されていない場合は、URLのパスコンポーネントのオブジェクトが使用されます。 他のレイヤーのデフォルト値はありません。

## 関連項目 {#section-e467e03330564796932ac081f1c9c1d0}

[&#x200B; カタログ：：パス &#x200B;](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md)、[属性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)、[&#x200B; テキスト=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f)、[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)、[&#x200B; マスク=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)、[&#x200B; オブジェクト &#x200B;](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)、[&#x200B; テンプレート &#x200B;](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)、[&#x200B; ネストと埋め込みのリクエスト &#x200B;](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
