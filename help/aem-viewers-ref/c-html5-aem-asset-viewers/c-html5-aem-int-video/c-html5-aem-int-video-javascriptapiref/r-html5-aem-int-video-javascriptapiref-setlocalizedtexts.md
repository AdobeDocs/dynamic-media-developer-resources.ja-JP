---
description: インタラクティブビデオビューアのJavaScript APIリファレンス。
seo-description: インタラクティブビデオビューアのJavaScript APIリファレンス。
seo-title: setLocalizedTexts
solution: Experience Manager
title: setLocalizedTexts
topic: Dynamic media
uuid: 11844a71-adb0-42a9-9b58-b69821070fd2
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# setLocalizedTexts{#setlocalizedtexts}

インタラクティブビデオビューアのJavaScript APIリファレンス。

` setLocalizedTexts( *`localizationInfo`*)`

1つ以上のロケールのローカリゼーションシンボル値を設定します。 このパラメーターは、前に呼び出す必要がありま `init()`す。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> localizationInfo <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p> { <span class="codeph"> Object </span>}ローカリゼーションデータを含むJSONオブジェクト。 </p> <p>詳しくは、ユ <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> ーザーインターフェイス要素のローカ </a> リゼーションを参照してください。 </p> <p>オブジェクトのコ <i>ンテンツについて詳しくは、ビューアSDK</i> User Guideおよび例も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

「 [init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)」も参照。

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"VideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played."},"fr":{"VideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus."},defaultLocale:"en"})
```

