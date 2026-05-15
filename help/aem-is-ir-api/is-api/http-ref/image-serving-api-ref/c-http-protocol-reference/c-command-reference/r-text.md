---
title: テキスト
description: レイヤーテキスト： テキストレイヤーのテキストと書式コンテンツを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3966b180-bef1-4fad-af71-ba42bbdffd59
TQID: 'https://experienceleague.adobe.com/ugojsTLZIxRW5mD7tyyCHZxGCYKrq1UuMkSsOn-Lc3k'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 172
ht-degree: 4%

---

# テキスト{#text}

レイヤーテキスト： テキストレイヤーのテキストと書式コンテンツを指定します。

` text= *`文字列`*`

<table id="simpletable_6C095D7F69874A8EA3D1D52103FA520C"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">文字列</span> </p> </td> 
  <td class="stentry"> <p>リッチテキスト形式（RTF）文字列またはプレーンテキスト文字列。 </p> </td> 
 </tr> 
</table>

すべてのフォント、フォントカラー、段落の書式設定は、RTF コマンドを使用して行います。 詳細については、[&#x200B; テキスト形式](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c)を参照してください。

`text=`は、`size=`で指定されたレイヤー長方形を塗りつぶすために、テキストの自動スケーリングをサポートしています。

[textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)を参照してください。

`text=`では、レンダリングされたテキストに合わせてテキストレイヤーのサイズを自動的に変更できます（`size=`が指定されていない場合、または幅のみが指定されている場合）。 この場合、RTF整列コマンド `\ql`、`\qr`、`\qc`のうち1つだけが適用される可能性があり、それ以外の場合はエラーが返されることに注意してください。

## プロパティ {#section-8c0f020094a44c6b858454ef91ab4edf}

レイヤー属性。 `layer=comp`の場合は`layer=0`に適用されます。 同じレイヤー内の`src=`と`textPs=`は相互に排他的です。最後に`text=`、`textPs=`、`src=`が優先され、これが画像レイヤーかテキストレイヤーかを判断します。 エフェクトレイヤーでは無視されます。

## 初期設定 {#section-58958671e0ad479e8d5f6c1d41d7dc74}

なし

## 例 {#section-d011f765ec5c418d814a821019b0eef0}

[&#x200B; テンプレート &#x200B;](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)の[&#x200B; テキスト形式](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c)および[例A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac)の例を参照してください。

## 関連項目 {#section-207b779ab67342a5acd343e6bcc749c4}

[&#x200B; テキストの書式設定](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c)、[&#x200B; テキストの配置](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87)、[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)、[textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)、[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
