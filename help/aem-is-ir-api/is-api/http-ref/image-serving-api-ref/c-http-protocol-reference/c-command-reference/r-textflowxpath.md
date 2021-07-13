---
description: テキストフローの除外領域。 テキストフローから除外する1つ以上の領域を指定します。
solution: Experience Manager
title: textFlowXPath
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 2430ab43-c032-4c2f-93c3-225e8116f100
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 8%

---

# textFlowXPath{#textflowxpath}

テキストフローの除外領域。 テキストフローから除外する1つ以上の領域を指定します。

`textFlowXPath= *`pathDefinition`*`

<table id="simpletable_7E0EA48AEBB5426CBE948FCA18882C66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>Path data. </p></td> 
 </tr> 
</table>

[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)を参照してください。*`pathDefinition`*&#x200B;の説明も含まれます。 パス定義が指定されていない場合、`textFlowXPath=`は無視されます。

## プロパティ {#section-cd1ebb151d4a405fbfc508d46522d686}

テキストレイヤー属性（`textPs=`のみ）。 他のレイヤーでは無視され、`textFlowPath=`を付けずに指定した場合は無視されます。 `layer=comp`に対して指定された場合、`layer=0`に適用されます。

## 初期設定 {#section-9405cda904684d829ed12a9e40a4dc46}

なし

## 関連項目 {#section-855228e744c7437a921d5db5b24bcd95}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) 、  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)、  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)
