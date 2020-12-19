---
description: レイヤーテキスト(Adobe Photoshop互換) テキストレイヤーのテキスト本文を指定します。
seo-description: レイヤーテキスト(Adobe Photoshop互換) テキストレイヤーのテキスト本文を指定します。
seo-title: textPs
solution: Experience Manager
title: textPs
topic: Scene7 Image Serving - Image Rendering API
uuid: 45e587b6-8dc8-408c-ade6-d70025fd1117
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 4%

---


# textPs{#textps}

レイヤーテキスト(Adobe Photoshop互換) テキストレイヤーのテキスト本文を指定します。

`textPs= *`文字列`*`

<table id="simpletable_4E2D08FD4EEC4EDC9EFE9F6F2E22DB0C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> string</span> </span> </p> </td> 
  <td class="stentry"> <p>リッチテキスト形式(RTF)文字列。 </p></td> 
 </tr> 
</table>

すべてのフォント、フォント色、段落の書式設定は、RTFコマンドを使用して制御できます。

「[テキストの書式設定](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c)」を参照してください。

`textPs=` は、位置合わせ、および/またはで定義された非長方形領域へのテキストの流し込み、およびで定義された任意のパスに沿ったテキストのレンダリングなど、拡張機能 `textFlowPath=` をサポートしてい `textFlowXPath=` `textPath=`ます。

## プロパティ {#section-a289dc26b6534b41998b1e241d5f2f92}

レイヤー属性。 `layer=comp`の場合は`layer=0`に適用されます。 同じレイヤー内の`src=`と`text=`は相互に排他的です。 `text=`、`textPs=`、および`src=`の最後の値が使用され、これが画像かテキストレイヤーかが判断されます。 エフェクトレイヤーでは無視されます。

## 初期設定 {#section-11c2ae2c96d64a0a9c207252df663e4d}

なし

## 関連項目 {#section-5c2b25767d2b47b5be817271ab12e13c}

[Text Formatting](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c),  [src=, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)textAttr=text,  [text=text](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d),  [text=text, text Flow Path=textFlow FlowtextFlow Flow Flow Path=Xp, text Path=Text Formatting Src=, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowxpath.md#reference-c55d4e41a28f40aca6a24ca218c28542) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd) [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15)
