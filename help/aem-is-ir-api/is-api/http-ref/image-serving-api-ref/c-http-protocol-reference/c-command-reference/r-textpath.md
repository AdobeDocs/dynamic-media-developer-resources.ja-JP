---
title: textPath
description: テキストパス。 textPs=で指定したテキストのベースラインとして使用するパスを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1c515786-bbba-44d3-837e-b474af293b7e
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---

# textPath{#textpath}

テキストパス。 textPs=で指定したテキストのベースラインとして使用するパスを指定します。

textPath= *`pathDefinition`*

<table id="simpletable_74F549E8625B483A9B334B24A7EB6D22"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 定義 </span> </p> </td> 
  <td class="stentry"> <p>パスデータ。 </p></td> 
 </tr> 
</table>

詳細（[ の説明など）については、](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)clipPath=*`pathDefinition`* を参照してください。

>[!NOTE]
>
>`clipPath=` とは異なり、「z」または「Z」がサブパスの最後に指定されていない場合、テキストパスは自動的に閉じません。

複数 *`pathDefinition`* サブパスを含めることができます。 テキストは、指定された順序でサブパス上にレンダリングされます。

RTF コマンド `\ql`、`\qc`、`\qr`、`\li`、`\ri` を使用して、レンダリングされたテキストをパスに沿って配置できます。

## プロパティ {#section-068137df436c46b9b55d271eb60e7285}

テキストレイヤー属性（`textPs=` のみ）。 他のレイヤーで無視されます。 `layer=0` に対して指定されている場合は、`layer=comp` に適用されます。 `textPs=` が存在する場合、無視されます。

レイヤーに `textPath=` と `textFlowPath=` の両方が含まれる場合は、エラーが返されます。

## 初期設定 {#section-697b1f2cfc43498080a31327e6eb173d}

なし（標準テキストレンダリングの場合）。

## 関連項目 {#section-3050d8f47e1d4f5c9b474dece45ea93d}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) , [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), [ テキストレイヤー ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
