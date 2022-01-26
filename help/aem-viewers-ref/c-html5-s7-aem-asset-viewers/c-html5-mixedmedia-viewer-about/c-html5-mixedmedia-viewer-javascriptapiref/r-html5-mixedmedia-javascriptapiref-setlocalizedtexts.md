---
title: setLocalizedTexts
description: 混在メディアビューアの JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 19bc61be-4321-434a-ae2c-4576c7799c0a
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 2%

---

# setLocalizedTexts{#setlocalizedtexts}

混在メディアビューアの JavaScript API リファレンス。

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> {<span class="codeph"> オブジェクト</span>} ローカリゼーションデータを含む JSON オブジェクト。 </p> <p>詳しくは、 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1" format="dita" scope="local"> ユーザーインターフェイス要素のローカライゼーション</a> を参照してください。 </p> <p>関連トピック <i>ビューア SDK ユーザーガイド</i> と例を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

1 つ以上のロケールのローカライゼーション SYMBOL 値を設定します。 このパラメーターは、の前に呼び出す必要があります `init()`.

関連トピック [init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```
