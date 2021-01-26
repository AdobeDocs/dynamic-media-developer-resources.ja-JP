---
description: テキストフロー領域 textPs=で指定したテキストをフローする1つ以上の領域を指定します。
seo-description: テキストフロー領域 textPs=で指定したテキストをフローする1つ以上の領域を指定します。
seo-title: textFlowPath
solution: Experience Manager
title: textFlowPath
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 5449d78f-e56b-4afb-a05a-7cf8f1f37278
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 5%

---


# textFlowPath{#textflowpath}

テキストフロー領域 textPs=で指定したテキストをフローする1つ以上の領域を指定します。

` textFlowPath= *`pathDefinition`*`

<table id="simpletable_52CEFF5C3CCB4642A9A320D01B1BF8E0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pathDefinition  </span> </p> </td> 
  <td class="stentry"> <p>Path data. </p> </td> 
 </tr> 
</table>

*`pathDefinition`*&#x200B;の説明を含む詳細については、[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)を参照してください。

`textFlowPath=`が存在する場合、RTF余白コマンド`\margl`、`\margr`、`\margt`、`\margb`は無視されます。 パス定義が指定されていない場合、`textFlowPath=`は無視されます。

## プロパティ {#section-b68dc887c6534ce8982cad740b3aeaa4}

テキストレイヤー属性（`textPs=`のみ） 他のレイヤーでは無視されます。 `layer=comp`に対して指定した場合、`layer=0`に適用されます。

## 初期設定 {#section-68c4559b9e8242059b82e5a39a455dfc}

レイヤーの長方形と同じ。テキストは、レイヤーの長方形全体を塗りつぶします。

## 関連項目 {#section-592b0039cf99471188db6a7df44b450a}

[textPs=、](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) clipPath= [、](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)textFlowPath= [、textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)、 [textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15) [、ledTextLayers](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
