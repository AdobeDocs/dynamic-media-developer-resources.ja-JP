---
title: テキスト
description: レイヤーテキスト。 テキストレイヤーのテキストと書式設定コンテンツを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3966b180-bef1-4fad-af71-ba42bbdffd59
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 4%

---

# テキスト{#text}

レイヤーテキスト。 テキストレイヤーのテキストと書式設定コンテンツを指定します。

` text= *` 文字列 `*`

<table id="simpletable_6C095D7F69874A8EA3D1D52103FA520C"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> string </span> </p> </td> 
  <td class="stentry"> <p>リッチテキスト形式（RTF）の文字列またはプレーンテキストの文字列。 </p> </td> 
 </tr> 
</table>

フォント、フォントカラー、段落書式のすべての制御は、RTF コマンドを使用して実現されます。 詳しくは、[ テキストの書式設定 ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) を参照してください。

`text=` では、`size=` で指定したレイヤーの長方形を埋めるためのテキストの自動スケーリングがサポートされています。

[textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d) を参照。

`text=` は、レンダリングされたテキストに合わせてテキストレイヤーのサイズを自動的に調整できます（`size=` が指定されていない場合、または幅のみが指定されている場合）。 この場合、RTF 整列コマンド `\ql`、`\qr`、`\qc` のいずれか 1 つのみ適用されることに注意してください。それ以外の場合は、エラーが返されます。

## プロパティ {#section-8c0f020094a44c6b858454ef91ab4edf}

レイヤー属性。 `layer=0` の場合は `layer=comp` に適用されます。 同じレイヤー内で `src=` と `textPs=` を相互に排他的です。最後に出現する `text=`、`textPs=` および `src=` が優先され、これが画像レイヤーかテキストレイヤーかを判断します。 エフェクトレイヤーで無視されます。

## 初期設定 {#section-58958671e0ad479e8d5f6c1d41d7dc74}

なし

## 例 {#section-d011f765ec5c418d814a821019b0eef0}

[ テキストの書式設定 ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) の例および [ テンプレート ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) の [ 例 A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) を参照してください。

## 関連項目 {#section-207b779ab67342a5acd343e6bcc749c4}

[ テキストの書式設定 ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c), [ テキストの配置 ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
