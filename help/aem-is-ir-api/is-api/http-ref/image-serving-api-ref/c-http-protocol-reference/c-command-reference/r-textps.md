---
title: textPs
description: レイヤーテキスト (Adobe Photoshop互換 ) テキストレイヤーのテキスト本文を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 95f343ce-bea3-425e-9a25-d1d141a976d9
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 4%

---

# textPs{#textps}

レイヤーテキスト (Adobe Photoshop互換 ) テキストレイヤーのテキスト本文を指定します。

`textPs= *`文字列`*`

<table id="simpletable_4E2D08FD4EEC4EDC9EFE9F6F2E22DB0C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 文字列</span> </span> </p> </td> 
  <td class="stentry"> <p>リッチテキスト形式 (RTF) の文字列。 </p></td> 
 </tr> 
</table>

すべてのフォント、フォントカラー、段落書式設定コントロールは、RTF コマンドを使用して実現します。

詳しくは、 [テキストの書式設定](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c).

`textPs=` は、位置合わせや、で定義された長方形以外の領域へのテキストの流し込みなど、拡張機能をサポートします。 `textFlowPath=` および/または `textFlowXPath=`、およびで定義された任意のパスに沿ったテキストのレンダリング `textPath=`.

## プロパティ {#section-a289dc26b6534b41998b1e241d5f2f92}

レイヤー属性。 適用先 `layer=0` if `layer=comp`. と相互に排他的 `src=` および `text=` を同じレイヤーに含めます。 最後に発生した `text=`, `textPs=`、および `src=` を使用し、画像かテキストレイヤーかを判断します。 効果画層で無視されます。

## 初期設定 {#section-11c2ae2c96d64a0a9c207252df663e4d}

なし

## 関連項目 {#section-5c2b25767d2b47b5be817271ab12e13c}

[テキストの書式設定](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), [textFlowXPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowxpath.md#reference-c55d4e41a28f40aca6a24ca218c28542), [textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd), [textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15)
