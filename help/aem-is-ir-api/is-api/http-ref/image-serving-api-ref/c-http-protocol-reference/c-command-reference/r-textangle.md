---
description: テキストのレンダリング方向 textPs=で指定したテキストがレイアウトされ、テキストボックスにレンダリングされる角度を指定します（size=またはtextFlowPath=で定義）。
seo-description: テキストのレンダリング方向 textPs=で指定したテキストがレイアウトされ、テキストボックスにレンダリングされる角度を指定します（size=またはtextFlowPath=で定義）。
seo-title: textAngle
solution: Experience Manager
title: textAngle
topic: Scene7 Image Serving - Image Rendering API
uuid: ac54c186-1fc5-479a-89f2-ff2da5e7999a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# textAngle{#textangle}

テキストのレンダリング方向 textPs=で指定したテキストがレイアウトされ、テキストボックスにレンダリングされる角度を指定します（size=またはtextFlowPath=で定義）。

` textAngle= *`角度`*`

<table id="simpletable_40832AC4B43A458CA69B225768124F58"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 角度 </span> </p> </td> 
  <td class="stentry"> <p>方向角（度） </p> </td> 
 </tr> 
</table>

正の値を指定すると、テキストが時計回りに回転します。テキスト `textAngle=90` を上から下に描画します。

## プロパティ {#section-6d586a632daa4261a8ce62db56140b36}

レイヤー属性。 ifに適 `layer=0` 用されま `layer=comp`す。 このレイヤーに対 `textPs=` してが指定されていない場合、またはが指定されている場合 `textPath=` は無視されます。

## 初期設定 {#section-49a9f5819c994c27928282c14b2bb2a7}

`textAngle=0` 回転なし。

## 関連項目 {#section-dccc29ff33704061b2519b56b7be45fd}

[Text Formatting](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c), [Text Positioning](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87), [textPs=textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)[textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd)
