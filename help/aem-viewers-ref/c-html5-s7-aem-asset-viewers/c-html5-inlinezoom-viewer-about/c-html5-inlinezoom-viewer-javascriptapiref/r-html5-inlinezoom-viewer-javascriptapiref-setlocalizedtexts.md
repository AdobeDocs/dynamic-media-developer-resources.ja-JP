---
description: インラインズームビューアのJavaScript APIリファレンス。
solution: Experience Manager
title: setLocalizedTexts
feature: Dynamic Media Classic，ビューア，SDK/API，インラインズーム
role: Developer,Business Practitioner
exl-id: a0d602f5-e698-4dad-af95-70ef5ef88af6
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 2%

---

# setLocalizedTexts{#setlocalizedtexts}

インラインズームビューアのJavaScript APIリファレンス。

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo  </span> </span> </p> </td> 
   <td colname="col2"> <p> { <span class="codeph"> Object </span>} JSONオブジェクトとローカリゼーションデータ。 </p> <p>詳しくは、 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27" format="dita" scope="local">ユーザーインターフェイス要素のローカライゼーション</a>を参照してください。 </p> <p>オブジェクトのコンテンツについて詳しくは、『<i>ビューアSDKユーザーガイド</i>』と例を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

1つ以上のロケールのローカライゼーションシンボルの値を設定します。 このパラメーターは、`init()`の前に呼び出す必要があります。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)も参照してください。

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom"},"fr":{"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer"},defaultLocale:"en"})
```
