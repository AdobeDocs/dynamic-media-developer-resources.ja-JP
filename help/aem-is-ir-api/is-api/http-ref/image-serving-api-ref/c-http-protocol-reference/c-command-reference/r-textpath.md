---
description: テキストパス textPs=で提供されるテキストのベースラインとして使用するパスを指定します。
seo-description: テキストパス textPs=で提供されるテキストのベースラインとして使用するパスを指定します。
seo-title: textPath
solution: Experience Manager
title: textPath
topic: Scene7 Image Serving - Image Rendering API
uuid: a2f0047b-ad62-4605-a723-b43d53fbea56
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 3%

---


# textPath{#textpath}

テキストパス textPs=で提供されるテキストのベースラインとして使用するパスを指定します。

textPath= *`pathDefinition`*

<table id="simpletable_74F549E8625B483A9B334B24A7EB6D22"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>Path data. </p></td> 
 </tr> 
</table>

*`pathDefinition`*&#x200B;の説明を含む詳細については、[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)を参照してください。

>[!NOTE]
>
>`clipPath=`とは異なり、サブパスの末尾で&#39;z&#39;または&#39;Z&#39;が指定されていない場合、テキストパスは自動的に閉じられません。

*`pathDefinition`* には、複数のサブパスを含めることができます。サブパス上のテキストは、指定された順序でレンダリングされます。

RTFコマンド`\ql`、`\qc`、`\qr`、`\li`、`\ri`を使用して、レンダリングされたテキストをパスに沿って配置できます。

## プロパティ {#section-068137df436c46b9b55d271eb60e7285}

テキストレイヤー属性（`textPs=`のみ） 他のレイヤーでは無視されます。 `layer=comp`に対して指定した場合、`layer=0`に適用されます。 `textPs=`が存在する場合は無視されます。

レイヤーに`textPath=`と`textFlowPath=`の両方が含まれる場合は、エラーが返されます。

## 初期設定 {#section-697b1f2cfc43498080a31327e6eb173d}

なし（標準のテキストレンダリング用）。

## 関連項目 {#section-3050d8f47e1d4f5c9b474dece45ea93d}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) 、 [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)、 [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)、 [テキストレイヤー](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
