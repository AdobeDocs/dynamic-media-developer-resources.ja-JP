---
description: 合成テンプレート メインカタログ以外のカタログにある合成テンプレートを指定できます。
solution: Experience Manager
title: テンプレート
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: ddfccb4ca157764e39fc719d96b63e6ee95304bf
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 6%

---


# テンプレート{#template}

合成テンプレート メインカタログ以外のカタログ内の合成テンプレートを指定できます。

`template= *`テンプレート`*`

<table id="simpletable_DEC6F4EB460D453B8F272C98C9C8B7E5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> オブジェクト</span> </p> </td> 
  <td class="stentry"> <p>テンプレート. </p></td> 
 </tr> 
</table>

*`template`* は、テンプレート本体がに含まれる画像カタログエントリである必要があり `catalog::Modifier`ます。

`template=`が存在する場合、要求パスで指定されたオブジェクトは、レイヤー0のソースとして適用されません。 ただし、事前定義されたパス変数`$object$`を`src=`値として使用することで、テンプレート内の任意の場所で`src=`または`mask=`として参照できます。 `catalog::Modifier` の値は、常に適用されるのに対し、リクエストパスで指定されたオブジェクトは、テンプレート `$object$` 内ののの置き換えでのみ適用 `catalog::PostModifier` されます。

レイヤー0は、テンプレート本体で定義され、画像、べた塗り、テキスト、入れ子または埋め込みの要求レイヤーのいずれかになります。

`catalog:PostModifier` の値 *`object`* は、で使用 *`object`* する場合は無視され `template=`ます。

## 初期設定 {#section-9de53ea27c4b4fd4811e40e345d8ba05}

なし

## プロパティ {#section-daf3afb1d09c45a6a394468d0874c439}

要求属性。 現在のレイヤー設定に関係なく適用されます。

## 例 {#section-9a4f260ed43342b186b0fe855f34bca6}

[テンプレート](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)の例を参照してください。

## 関連項目 {#section-067587444f774469931ecafd5a39834c}

[オブジェクト](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0), [テンプレート](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [定義済みのパス変数](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)
