---
description: レイヤーのテキスト テキストレイヤーのテキストと書式の内容を指定します。
seo-description: レイヤーのテキスト テキストレイヤーのテキストと書式の内容を指定します。
seo-title: テキスト
solution: Experience Manager
title: テキスト
topic: Scene7 Image Serving - Image Rendering API
uuid: 5b4f9282-83a3-488d-b5d2-deb2c92de564
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# テキスト{#text}

レイヤーのテキスト テキストレイヤーのテキストと書式の内容を指定します。

` text= *`文字列`*`

<table id="simpletable_6C095D7F69874A8EA3D1D52103FA520C"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 文字列 </span> </p> </td> 
  <td class="stentry"> <p>リッチテキスト形式(RTF)の文字列またはプレーンテキストの文字列。 </p> </td> 
 </tr> 
</table>

すべてのフォント、フォントカラー、段落の書式設定は、RTFコマンドを使用して制御できます。 詳しくは、「テキ [ストの書式設定](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) 」を参照してください。

`text=` では、で指定したレイヤーの長方形を埋めるためのテキストの自動拡大縮小をサポートしていま `size=`す。

textAttr= [を参照](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)。

`text=` は、レンダリングされたテキストに合わせて、テキストレイヤーのサイズを自動的に調整できます( `size=` が指定されていない場合、または幅のみが指定されている場合)。 この場合、RTF整列コマンドの1つ、およびを適 `\ql`用で `\qr`きるこ `\qc` とに注意してください。それ以外の場合は、エラーが返されます。

## プロパティ {#section-8c0f020094a44c6b858454ef91ab4edf}

レイヤー属性。 ifに適 `layer=0` 用されま `layer=comp`す。 同じ層内で `src=` 互い `textPs=` に排他的で、、、およびの最後 `text=`の値が `textPs=`使用され `src=` 、画像かテキストレイヤーかが決まります。 エフェクトレイヤーでは無視されます。

## 初期設定 {#section-58958671e0ad479e8d5f6c1d41d7dc74}

なし

## 例 {#section-d011f765ec5c418d814a821019b0eef0}

「テキストの書式設定 [」の例と](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) 「テンプレ [ートの例](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) A [」を参照](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)してください。

## 関連項目 {#section-207b779ab67342a5acd343e6bcc749c4}

[Text Formatting](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c), [Text Positioning](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
