---
title: テンプレート
description: 合成テンプレート。 メイン カタログ以外のカタログにある合成テンプレートを指定できます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 56ebf2a1-f2c3-4b3f-8d0a-9383f1411440
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 4%

---

# テンプレート{#template}

合成テンプレート。 メイン カタログ以外のカタログ内の合成テンプレートを指定できます。

`template= *` テンプレート `*`

<table id="simpletable_DEC6F4EB460D453B8F272C98C9C8B7E5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> オブジェクト </span> </p> </td> 
  <td class="stentry"> <p>テンプレート。 </p></td> 
 </tr> 
</table>

*`template`* は、`catalog::Modifier` に含まれるテンプレート本文を持つ画像カタログエントリである必要があります。

`template=` が存在する場合、リクエストパスで指定されたオブジェクトはレイヤー 0 のソースとして適用されません。 ただし、定義済みのパス変数 `$object$` を `src=` ール値として使用することで、テンプレート内のどこからでも `src=` または `mask=` として参照できます。 リクエストパスで指定されたオブジェクトの `catalog::Modifier` は、テンプレート内の `$object$` の置換でのみ適用されますが、`catalog::PostModifier` は常に適用されます。

レイヤー 0 は、テンプレート本文で定義され、画像、単色、テキスト、ネストされたリクエストレイヤーまたは埋め込まれたリクエストレイヤーにすることができます。

*`object`* を `template=` と共に使用する場合、*`object`* の `catalog:PostModifier` は無視されます。

## 初期設定 {#section-9de53ea27c4b4fd4811e40e345d8ba05}

なし

## プロパティ {#section-daf3afb1d09c45a6a394468d0874c439}

リクエスト属性。 現在のレイヤ設定に関係なく適用されます。

## 例 {#section-9a4f260ed43342b186b0fe855f34bca6}

[ テンプレート ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) の例を参照してください。

## 関連項目 {#section-067587444f774469931ecafd5a39834c}

[object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0), [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [ 定義済みのパス変数 ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)
