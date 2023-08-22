---
title: テンプレート
description: 合成テンプレート。 メインカタログ以外のカタログにある合成テンプレートを指定できます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 56ebf2a1-f2c3-4b3f-8d0a-9383f1411440
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 6%

---

# テンプレート{#template}

合成テンプレート。 メインカタログ以外のカタログで合成テンプレートを指定できます。

`template= *`テンプレート`*`

<table id="simpletable_DEC6F4EB460D453B8F272C98C9C8B7E5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> オブジェクト</span> </p> </td> 
  <td class="stentry"> <p>テンプレート. </p></td> 
 </tr> 
</table>

*`template`* は、テンプレート本文が `catalog::Modifier`.

条件 `template=` が存在する場合、要求パスで指定されたオブジェクトは、レイヤー 0 のソースとして適用されません。 ただし、 `src=` または `mask=` 事前定義済みのパス変数を使用して、テンプレート内の任意の場所に移動 `$object$` as a `src=` の値です。 `catalog::Modifier` リクエストパスで指定されたオブジェクトの `$object$` テンプレート内で、 `catalog::PostModifier` が常に適用されます。

レイヤー 0 は、テンプレート本体で定義され、画像、べた塗り、テキスト、ネストされたリクエストレイヤーまたは埋め込まれたリクエストレイヤーのいずれかになります。

`catalog:PostModifier` / *`object`* 次の場合は無視されます： *`object`* 次の場合に使用： `template=`.

## 初期設定 {#section-9de53ea27c4b4fd4811e40e345d8ba05}

なし

## プロパティ {#section-daf3afb1d09c45a6a394468d0874c439}

要求属性。 現在の画層設定に関係なく適用されます。

## 例 {#section-9a4f260ed43342b186b0fe855f34bca6}

詳しくは、 [テンプレート](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## 関連項目 {#section-067587444f774469931ecafd5a39834c}

[object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0), [テンプレート](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [事前定義されたパス変数](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)
