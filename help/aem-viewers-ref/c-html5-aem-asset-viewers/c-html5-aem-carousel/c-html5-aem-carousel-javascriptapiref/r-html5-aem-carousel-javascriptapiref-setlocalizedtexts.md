---
title: setLocalizedTexts
description: カルーセルビューアのJavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 8ffb8960-187a-43ab-8081-7dfd95d4c75d
source-git-commit: 96ac67e5645c2c55920cc971806ba2f14ae57044
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 2%

---

# setLocalizedTexts{#setlocalizedtexts}

カルーセルビューアのJavaScript API リファレンス。

` setLocalizedTexts( *`localizationInfo`*)`

1 つまたは複数のロケールの SYMBOL 値を設定します。 このパラメーターは、`init()` 前に呼び出す必要があります。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> ローカリゼーションデータを含む {<span class="codeph"> Object</span>} JSON オブジェクト。 </p> <p>詳 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-localization.md" format="dita" scope="local"> くは、ユーザーインターフェイス要素のローカライゼーショ </a> を参照してください。 </p> <p><i>Viewer SDK User Guide</i> も参照してください。また、オブジェクトのコンテンツに関する詳細については、例を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

[init](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b) も参照してください。

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"PanLeftButton.TOOLTIP":"Left"},"fr":{"PanLeftButton.TOOLTIP":"Gauchiste"},defaultLocale:"en"})
```
