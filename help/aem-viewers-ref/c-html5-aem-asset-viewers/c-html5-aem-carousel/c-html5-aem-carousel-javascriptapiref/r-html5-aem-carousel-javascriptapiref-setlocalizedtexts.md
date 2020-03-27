---
description: カルーセルビューアのJavaScript APIリファレンス。
seo-description: カルーセルビューアのJavaScript APIリファレンス。
seo-title: setLocalizedTexts
solution: Experience Manager
title: setLocalizedTexts
topic: Dynamic media
uuid: f69d3232-dd7c-41b5-87a0-146b8fb1bdb1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setLocalizedTexts{#setlocalizedtexts}

カルーセルビューアのJavaScript APIリファレンス。

` setLocalizedTexts( *`localizationInfo`*)`

1つ以上のロケールのローカリゼーションシンボル値を設定します。 このパラメーターは、前に呼び出す必要がありま `init()`す。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> localizationInfo <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p> {<span class="codeph"> Object</span>}ローカリゼーションデータを含むJSONオブジェクト。 </p> <p>詳しくは、ユ <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-localization.md" format="dita" scope="local"> ーザーインターフェイス要素のローカリゼーション</a> を参照してください。 </p> <p>オブジェクトのコ <i>ンテンツについて詳しくは、ビューアSDK</i> User Guideおよび例も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

「 [init](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)」も参照。

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"PanLeftButton.TOOLTIP":"Left"},"fr":{"PanLeftButton.TOOLTIP":"Gauchiste"},defaultLocale:"en"})
```

