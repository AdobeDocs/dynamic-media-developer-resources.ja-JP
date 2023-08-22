---
title: textFlowXPath
description: テキストフローの除外領域。 テキストフローから除外する 1 つ以上の領域を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2430ab43-c032-4c2f-93c3-225e8116f100
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 7%

---

# textFlowXPath{#textflowxpath}

テキストフローの除外領域。 テキストフローから除外する 1 つ以上の領域を指定します。

`textFlowXPath= *`pathDefinition`*`

<table id="simpletable_7E0EA48AEBB5426CBE948FCA18882C66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>Path data. </p></td> 
 </tr> 
</table>

詳しくは、 [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) 追加情報 ( *`pathDefinition`*. パス定義が指定されていない場合、 `textFlowXPath=` は無視されます。

## プロパティ {#section-cd1ebb151d4a405fbfc508d46522d686}

テキストレイヤー属性 ( `textPs=` のみ )。 他の画層で無視されるか、なしで指定された場合は無視されます `textFlowPath=`. 適用先 `layer=0` 指定されている場合 `layer=comp`.

## 初期設定 {#section-9405cda904684d829ed12a9e40a4dc46}

なし

## 関連項目 {#section-855228e744c7437a921d5db5b24bcd95}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) , [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)
