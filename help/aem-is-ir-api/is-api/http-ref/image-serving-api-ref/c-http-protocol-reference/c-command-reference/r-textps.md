---
title: textPs
description: レイヤーテキスト（Adobe Photoshop互換）。 テキストレイヤーのテキスト本文を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 95f343ce-bea3-425e-9a25-d1d141a976d9
TQID: 'https://experienceleague.adobe.com/z5z7-6Pe4B-DUsxcspNcMxS-gXXo8Cv7stwBEMpxnNo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 3%

---

# textPs{#textps}

レイヤーテキスト（Adobe Photoshop互換）。 テキストレイヤーのテキスト本文を指定します。

`textPs= *`文字列`*`

<table id="simpletable_4E2D08FD4EEC4EDC9EFE9F6F2E22DB0C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname">文字列</span> </span> </p> </td> 
  <td class="stentry"> <p>リッチテキストフォーマット（RTF）文字列。 </p></td> 
 </tr> 
</table>

すべてのフォント、フォントカラー、段落の書式設定は、RTF コマンドを使用して行います。

[ テキスト形式](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c)を参照してください。

`textPs=`は、位置合わせ、`textFlowPath=`および/または`textFlowXPath=`で定義された長方形以外の領域へのテキストの流れ、`textPath=`で定義された任意のパスに沿ったテキストのレンダリングなどの拡張機能をサポートしています。

## プロパティ {#section-a289dc26b6534b41998b1e241d5f2f92}

レイヤー属性。 `layer=comp`の場合は`layer=0`に適用されます。 同じレイヤーの`src=`および`text=`と相互排他的です。 `text=`、`textPs=`および`src=`の最後の出現が優先され、これが画像であるかテキストレイヤーであるかを判断します。 エフェクトレイヤーでは無視されます。

## 初期設定 {#section-11c2ae2c96d64a0a9c207252df663e4d}

なし

## 関連項目 {#section-5c2b25767d2b47b5be817271ab12e13c}

[ テキスト形式](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c)、[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)、[textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)、[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f)、[textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)、[textFlowXPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowxpath.md#reference-c55d4e41a28f40aca6a24ca218c28542)、[textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd)、[textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15)
