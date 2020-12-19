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
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 4%

---


# textAngle{#textangle}

テキストのレンダリング方向 textPs=で指定したテキストがレイアウトされ、テキストボックスにレンダリングされる角度を指定します（size=またはtextFlowPath=で定義）。

` textAngle= *`角度`*`

<table id="simpletable_40832AC4B43A458CA69B225768124F58"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 角度 </span> </p> </td> 
  <td class="stentry"> <p>方向角度（度） </p> </td> 
 </tr> 
</table>

正の値を指定すると、テキストは時計回りに回転します。`textAngle=90`はテキストを上から下に描画します。

## プロパティ {#section-6d586a632daa4261a8ce62db56140b36}

レイヤー属性。 `layer=comp`の場合は`layer=0`に適用されます。 このレイヤーに`textPs=`が指定されていない場合、または`textPath=`が指定されている場合は無視されます。

## 初期設定 {#section-49a9f5819c994c27928282c14b2bb2a7}

`textAngle=0` を返しません。

## 関連項目 {#section-dccc29ff33704061b2519b56b7be45fd}

[テキストの書式設定](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c)、 [テキストの配置](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87)、 [textPs=、](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)textFlowPath= [、](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)textPath=、 [thextPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd)
