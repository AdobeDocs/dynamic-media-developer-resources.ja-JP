---
title: textFlowPath
description: テキストフロー領域。 textPs=で指定したテキストをフローする 1 つ以上の領域を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b5575d17-150b-421c-b298-077b577eb95c
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 4%

---

# textFlowPath{#textflowpath}

テキストフロー領域。 textPs=で指定したテキストをフローする 1 つ以上の領域を指定します。

` textFlowPath= *`pathDefinition`*`

<table id="simpletable_52CEFF5C3CCB4642A9A320D01B1BF8E0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pathDefinition </span> </p> </td> 
  <td class="stentry"> <p>Path data. </p> </td> 
 </tr> 
</table>

詳しくは、 [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) 追加情報 ( *`pathDefinition`*.

RTF の margin コマンド `\margl`, `\margr`, `\margt`、および `\margb` 次の場合は無視されます： `textFlowPath=` が存在する。 パス定義が指定されていない場合、 `textFlowPath=` は無視されます。

## プロパティ {#section-b68dc887c6534ce8982cad740b3aeaa4}

テキストレイヤー属性 ( `textPs=` のみ )。 他の画層では無視されます。 適用先 `layer=0` 指定されている場合 `layer=comp`.

## 初期設定 {#section-68c4559b9e8242059b82e5a39a455dfc}

レイヤーの長方形と同じ。テキストはレイヤーの長方形全体を塗りつぶします。

## 関連項目 {#section-592b0039cf99471188db6a7df44b450a}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) , [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), [textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15), [テキストレイヤー](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
