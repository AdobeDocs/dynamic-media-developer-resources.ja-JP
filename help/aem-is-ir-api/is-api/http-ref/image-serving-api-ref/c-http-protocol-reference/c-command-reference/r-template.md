---
title: テンプレート
description: 合成テンプレート： メインカタログ以外のカタログにある合成テンプレートを指定できます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 56ebf2a1-f2c3-4b3f-8d0a-9383f1411440
TQID: 'https://experienceleague.adobe.com/O1v1LorIfXLyRso4ZRVJd7qx5A4kciWKVoG-df8q-Xg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 166
ht-degree: 4%

---

# テンプレート{#template}

合成テンプレート： メインカタログ以外のカタログで合成テンプレートを指定できます。

`template= *` テンプレート `*`

<table id="simpletable_DEC6F4EB460D453B8F272C98C9C8B7E5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> オブジェクト </span> </p> </td> 
  <td class="stentry"> <p>テンプレート： </p></td> 
 </tr> 
</table>

*`template`*&#x200B;は、`catalog::Modifier`に含まれるテンプレート本文を持つ画像カタログエントリである必要があります。

`template=`が存在する場合、要求パスで指定されたオブジェクトは、レイヤー0のソースとして適用されません。 ただし、定義済みのパス変数`$object$`を`src=`値として使用すると、テンプレート内の任意の場所で`src=`または`mask=`として参照できます。 リクエストパスで指定されたオブジェクトの`catalog::Modifier`は、テンプレート内の`$object$`の代用でのみ適用されますが、`catalog::PostModifier`は常に適用されます。

レイヤー0はテンプレート本文で定義され、画像、単色、テキスト、ネストまたは埋め込まれたリクエストレイヤーにすることができます。

*`object`*&#x200B;が`template=`と共に使用される場合、*`object`*&#x200B;件中`catalog:PostModifier`件は無視されます。

## 初期設定 {#section-9de53ea27c4b4fd4811e40e345d8ba05}

なし

## プロパティ {#section-daf3afb1d09c45a6a394468d0874c439}

リクエスト属性： 現在のレイヤー設定に関係なく適用されます。

## 例 {#section-9a4f260ed43342b186b0fe855f34bca6}

[ テンプレート ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)の例を参照してください。

## 関連項目 {#section-067587444f774469931ecafd5a39834c}

[ オブジェクト ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)、[ テンプレート ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)、[定義済みパス変数](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)
