---
title: setLocalizedTexts
description: 基本ズームビューアの JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 4472ac64-fdab-4f80-985a-29ed8537d235
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 2%

---

# setLocalizedTexts{#setlocalizedtexts}

基本ズームビューアの JavaScript API リファレンス。

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> {<span class="codeph"> オブジェクト</span>} ローカリゼーションデータを含む JSON オブジェクト。 </p> <p>詳しくは、 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> ユーザーインターフェイス要素のローカライゼーション</a> を参照してください。 </p> <p> 関連トピック <i>ビューア SDK ユーザーガイド</i> と例を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

1 つ以上のロケールのローカライゼーション SYMBOL 値を設定します。 このパラメーターは、の前に呼び出す必要があります `init()`.

関連トピック [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```
