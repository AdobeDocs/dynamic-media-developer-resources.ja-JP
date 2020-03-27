---
description: シャープ. シャープアトリビュート。レンダリング時にマテリアルにシャープを適用するタイミングを指定します。
seo-description: シャープ. シャープアトリビュート。レンダリング時にマテリアルにシャープを適用するタイミングを指定します。
seo-title: 'シャープ '
solution: Experience Manager
title: 'シャープ '
topic: Scene7 Image Serving - Image Rendering API
uuid: f153f496-f2c5-43d0-a7f0-00045fd96af8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# シャープ {#sharp}

シャープ. シャープアトリビュート。レンダリング時にマテリアルにシャープを適用するタイミングを指定します。

シャープの適用の種類と量は、ビネットによって、初期設定のマテリアルテンプレートを使用するか、を使用して制御しま `catalog::RenderSettings`す。

## プロパティ {#section-aac81b1a611b4bca90b8544eae7896df}

列挙。

<table id="simpletable_D52B41A39E4E4E54A06821B9D689DB30"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>シャープなし。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>通常のシャープ（変換後） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>別のシャープの適用（変換前） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>よりシャープにする（変換の前と後の両方）。 </p></td> 
 </tr> 
</table>

べた塗りのマテリアルでは無視され、その他のマテリアルではオプションです。

## 初期設定 {#section-a6bc204d552b4cc3ae6a77ec232c26ff}

`attribute::Sharpening` が使用されるのは、フィールドが存在しない場合、空の場合、または値がサポートされている選択肢の1つでない場合です。

## 関連項目 {#section-b462f9ad9ae347e1a1993abf2f2daa8e}

[attribute::Sharpening](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-sharp.md#reference-c706450cf95347f98f86c696f9167297) , [catalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rendersettings.md#reference-f3ae5e18095d40b2a8edef957dd82fbd), [sharp=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a)
