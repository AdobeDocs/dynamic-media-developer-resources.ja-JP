---
description: 反転されたレイヤークリップパス 現在のレイヤーの除外クリップパスを指定します。 clipXPath=で定義された領域内にあるレイヤーの部分はすべて透明にレンダリングされます。
seo-description: 反転されたレイヤークリップパス 現在のレイヤーの除外クリップパスを指定します。 clipXPath=で定義された領域内にあるレイヤーの部分はすべて透明にレンダリングされます。
seo-title: clipXPath
solution: Experience Manager
title: clipXPath
topic: Scene7 Image Serving - Image Rendering API
uuid: a4062f3f-5dba-4514-acde-e1b7d608a2e9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# clipXPath{#clipxpath}

反転されたレイヤークリップパス 現在のレイヤーの除外クリップパスを指定します。 clipXPath=で定義された領域内にあるレイヤーの部分はすべて透明にレンダリングされます。

`clipXPath= *`pathDefinition`*`

`clipXPathE= *`pathNamepathName`*&#42;[, *``*]`

<table id="simpletable_27AFC3A694874CF8B673460820EFD90D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span></span> </p> </td> 
  <td class="stentry"> <p>Path data. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span></span> </p> </td> 
  <td class="stentry"> <p>レイヤーソース画像に埋め込まれたパスの名前（ASCIIのみ）。 </p></td> 
 </tr> 
</table>

pathNameと [pathDefinitionの説明を含む詳細については、](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) clipPath= ` *`を参照し`*` てく ` *`ださい`*`。

## プロパティ {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

レイヤー属性。 現在のレイヤーまたは合成画像（の場合）に適用されま `layer=comp`す。 が指定されていな `clipPath=` い場合は無視されます。 エフェクトレイヤーでは無視されます。

## 初期設定 {#section-d1986aa31af14767aeb1b4a57add67f4}

なし

## 関連項目 {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
