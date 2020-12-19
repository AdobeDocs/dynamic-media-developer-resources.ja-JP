---
description: 基本ズームビューアのJavaScript APIリファレンス。
seo-description: 基本ズームビューアのJavaScript APIリファレンス。
seo-title: setLocalizedTexts
solution: Experience Manager
title: setLocalizedTexts
topic: Dynamic media
uuid: 34a2ea4e-5493-41fa-92bf-5cebe66f6370
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 2%

---


# setLocalizedTexts{#setlocalizedtexts}

基本ズームビューアのJavaScript APIリファレンス。

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> {<span class="codeph"> Object</span>} JSONオブジェクトとローカライゼーションデータ。 </p> <p>詳しくは、<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local">ローカライゼーションのユーザインターフェイス要素</a>を参照してください。 </p> <p> オブジェクトのコンテンツについて詳しくは、『<i>ビューアSDKユーザガイド</i>』および例も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

1つ以上のロケールに対してローカライゼーション記号の値を設定します。 このパラメーターは`init()`の前に呼び出す必要があります。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)も参照してください。

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101}を返す

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```

