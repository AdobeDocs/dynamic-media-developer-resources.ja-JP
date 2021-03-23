---
description: カルーセルビューアのJavaScript APIリファレンス。
seo-description: カルーセルビューアのJavaScript APIリファレンス。
seo-title: setLocalizedTexts
solution: Experience Manager
title: setLocalizedTexts
uuid: f69d3232-dd7c-41b5-87a0-146b8fb1bdb1
feature: Dynamic Mediaクラシック，ビューア，SDK/API，カルーセルバナー
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 2%

---


# setLocalizedTexts{#setlocalizedtexts}

カルーセルビューアのJavaScript APIリファレンス。

` setLocalizedTexts( *`localizationInfo`*)`

1つ以上のロケールに対してローカライゼーション記号の値を設定します。 このパラメーターは`init()`の前に呼び出す必要があります。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> {<span class="codeph"> Object</span>} JSONオブジェクトとローカライゼーションデータ。 </p> <p>詳しくは、<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-localization.md" format="dita" scope="local">ローカライゼーションのユーザインターフェイス要素</a>を参照してください。 </p> <p>オブジェクトのコンテンツについて詳しくは、『<i>ビューアSDKユーザガイド</i>』および例も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

[init](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)も参照してください。

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101}を返す

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"PanLeftButton.TOOLTIP":"Left"},"fr":{"PanLeftButton.TOOLTIP":"Gauchiste"},defaultLocale:"en"})
```

