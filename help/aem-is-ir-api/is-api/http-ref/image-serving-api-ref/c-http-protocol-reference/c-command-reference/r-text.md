---
title: テキスト
description: レイヤーテキスト。 テキストレイヤーのテキストおよびコンテンツの書式設定を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3966b180-bef1-4fad-af71-ba42bbdffd59
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 5%

---

# テキスト{#text}

レイヤーテキスト。 テキストレイヤーのテキストおよびコンテンツの書式設定を指定します。

` text= *`文字列`*`

<table id="simpletable_6C095D7F69874A8EA3D1D52103FA520C"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 文字列 </span> </p> </td> 
  <td class="stentry"> <p>リッチテキスト形式 (RTF) の文字列またはプレーンテキストの文字列。 </p> </td> 
 </tr> 
</table>

すべてのフォント、フォントカラー、段落書式設定コントロールは、RTF コマンドを使用して実現します。 参照： [テキストの書式設定](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) を参照してください。

`text=` は、で指定したレイヤの長方形を埋めるために、テキストの自動スケーリングをサポートします。 `size=`.

詳しくは、 [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d).

`text=` は、レンダリングされたテキストに合わせてテキストレイヤーのサイズを自動調整する ( `size=` が指定されていない場合、または幅のみが指定されている場合は。 この場合、RTF 整列コマンドは 1 つだけです。 `\ql`, `\qr`、および `\qc` が適用される場合があります。それ以外の場合はエラーが返されます。

## プロパティ {#section-8c0f020094a44c6b858454ef91ab4edf}

レイヤー属性。 適用先 `layer=0` if `layer=comp`. と相互に排他的 `src=` および `textPs=` 同じレイヤー内で、 `text=`, `textPs=`、および `src=` を使用し、画像かテキストレイヤーかを判断します。 効果画層で無視されます。

## 初期設定 {#section-58958671e0ad479e8d5f6c1d41d7dc74}

なし

## 例 {#section-d011f765ec5c418d814a821019b0eef0}

詳しくは、 [テキストの書式設定](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) および [例 A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) in [テンプレート](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## 関連項目 {#section-207b779ab67342a5acd343e6bcc749c4}

[テキストの書式設定](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c), [テキストの配置](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
