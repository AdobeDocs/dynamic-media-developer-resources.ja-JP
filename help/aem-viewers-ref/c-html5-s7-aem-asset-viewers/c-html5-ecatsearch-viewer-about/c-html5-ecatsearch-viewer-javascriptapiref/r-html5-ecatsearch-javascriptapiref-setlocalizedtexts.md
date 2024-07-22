---
description: ビデオビューア用のJavaScript API リファレンス。
solution: Experience Manager
title: setLocalizedTexts
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: dfd57bde-70cd-483f-bcd4-680186e4a733
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 2%

---

# setLocalizedTexts{#setlocalizedtexts}

ビデオビューア用のJavaScript API リファレンス。

[!DNL ` setLocalizedTexts( *`localizationInfo`*)`]

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> ローカリゼーションデータを含む {<span class="codeph"> Object</span>} JSON オブジェクト。 </p> <p>詳 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> くは、ユーザーインターフェイス要素のローカライゼーショ </a> を参照してください。 </p> <p><i>Viewer SDK User Guide</i> も参照してください。また、オブジェクトのコンテンツに関する詳細については、例を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

1 つまたは複数のロケールの SYMBOL 値を設定します。 このパラメーターは、[!DNL `init()`] 前に呼び出す必要があります。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b) も参照してください。

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```
