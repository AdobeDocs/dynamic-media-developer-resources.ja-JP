---
description: 合成テンプレート メインカタログ以外のカタログにある合成テンプレートを指定できます。
seo-description: 合成テンプレート メインカタログ以外のカタログにある合成テンプレートを指定できます。
seo-title: テンプレート
solution: Experience Manager
title: テンプレート
topic: Scene7 Image Serving - Image Rendering API
uuid: 59b37d60-1d0c-4d0b-a5a0-98d8bf9e9064
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# テンプレート{#template}

合成テンプレート メインカタログ以外のカタログにある合成テンプレートを指定できます。

`template= *`テンプレート`*`

<table id="simpletable_DEC6F4EB460D453B8F272C98C9C8B7E5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> オブジェクト</span> </p> </td> 
  <td class="stentry"> <p>テンプレート. </p></td> 
 </tr> 
</table>

*`template`* は、に含まれるテンプレート本体を持つ画像カタログエントリである必要がありま `catalog::Modifier`す。

が存在 `template=` する場合、要求パスで指定されたオブジェクトはレイヤー0のソースとして適用されませんが、事前定義されたパス変数を値として使用して、テンプレート内の `src=` 任意 `mask=` の場所やとして参照で `$object$` き `src=` ます。 `catalog::Modifier` の値は、常に適用されるのに対し、要求パスで指定されたオブジェクトは、テンプレート内のの置き換え `$object$` に関連してのみ適 `catalog::PostModifier` 用されます。

レイヤー0は、テンプレートの本体で定義され、画像、べた塗り、テキスト、ネストされたリクエストレイヤーまたは埋め込まれたリクエストレイヤーのいずれかです。

`catalog:PostModifier` をと共に *`object`* 使用した場合、 *`object`* の値は無視されま `template=`す。

## 初期設定 {#section-9de53ea27c4b4fd4811e40e345d8ba05}

なし

## プロパティ {#section-daf3afb1d09c45a6a394468d0874c439}

リクエスト属性。 現在のレイヤー設定に関係なく適用されます。

## 例 {#section-9a4f260ed43342b186b0fe855f34bca6}

テンプレートの例を参照して [ください](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)。

## 関連項目 {#section-067587444f774469931ecafd5a39834c}

[オブジェクト](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)、テ [ンプレート](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)、定義済み [パス変数](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)
