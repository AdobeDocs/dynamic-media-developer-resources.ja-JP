---
title: textPath
description: テキストパス。 textPs=で提供されるテキストのベースラインとして使用するパスを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1c515786-bbba-44d3-837e-b474af293b7e
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 4%

---

# textPath{#textpath}

テキストパス。 textPs=で提供されるテキストのベースラインとして使用するパスを指定します。

textPath= *`pathDefinition`*

<table id="simpletable_74F549E8625B483A9B334B24A7EB6D22"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>Path data. </p></td> 
 </tr> 
</table>

詳しくは、 [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) 追加情報 ( *`pathDefinition`*.

>[!NOTE]
>
>次と異なる `clipPath=`を指定した場合、サブパスの末尾に「z」または「Z」が指定されていない場合、テキストパスは自動的に閉じられません。

*`pathDefinition`* には複数のサブパスを含めることができます。 指定した順序でサブパスにテキストがレンダリングされます。

RTF コマンド `\ql`, `\qc`, `\qr`, `\li`、および `\ri` を使用して、レンダリングしたテキストをパスに沿って配置できます。

## プロパティ {#section-068137df436c46b9b55d271eb60e7285}

テキストレイヤー属性 ( `textPs=` のみ )。 他の画層では無視されます。 適用先 `layer=0` 指定されている場合 `layer=comp`. 次の場合は無視 `textPs=` が存在する。

画層に `textPath=` および `textFlowPath=`.

## 初期設定 {#section-697b1f2cfc43498080a31327e6eb173d}

なし（標準のテキストレンダリング用）。

## 関連項目 {#section-3050d8f47e1d4f5c9b474dece45ea93d}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) , [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), [テキストレイヤー](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
