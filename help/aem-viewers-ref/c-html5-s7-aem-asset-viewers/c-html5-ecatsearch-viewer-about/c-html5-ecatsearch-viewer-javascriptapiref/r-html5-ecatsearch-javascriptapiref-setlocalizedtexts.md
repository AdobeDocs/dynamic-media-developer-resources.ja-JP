---
description: ビデオビューアのJavaScript APIリファレンス。
solution: Experience Manager
title: setLocalizedTexts
feature: Dynamic Mediaクラシック，ビューア，SDK/API,eCatalog検索
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 2%

---


# setLocalizedTexts{#setlocalizedtexts}

ビデオビューアのJavaScript APIリファレンス。

[!DNL ` setLocalizedTexts( *`localizationInfo`*)`]

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> {<span class="codeph"> Object</span>} JSONオブジェクトとローカライゼーションデータ。 </p> <p>詳しくは、<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local">ローカライゼーションのユーザインターフェイス要素</a>を参照してください。 </p> <p>オブジェクトのコンテンツについて詳しくは、『<i>ビューアSDKユーザガイド</i>』および例も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

1つ以上のロケールに対してローカライゼーション記号の値を設定します。 このパラメーターは[!DNL `init()`]の前に呼び出す必要があります。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)も参照してください。

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101}を返す

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```

