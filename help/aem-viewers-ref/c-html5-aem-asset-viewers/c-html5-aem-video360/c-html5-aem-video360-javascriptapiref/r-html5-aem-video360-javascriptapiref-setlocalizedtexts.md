---
title: setLocalizedText
description: Video360 ViewerのJavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: b0434886-defa-47d4-9853-bfd73c64d036
TQID: 'https://experienceleague.adobe.com/oXnXBZeFmBHsA4JCdRKFaUo0TCU6g6hqXf97cz7-AHo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 69
ht-degree: 2%

---

# setLocalizedText{#setlocalizedtexts}

Video360 ViewerのJavaScript API リファレンス。

` setLocalizedTexts( *`localizationInfo`*)`

1つ以上のロケールのローカライズシンボル値を設定します。 このパラメーターは`init()`の前に呼び出す必要があります。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo </span> </span> </p> </td> 
   <td colname="col2"> <p> { <span class="codeph"> オブジェクト </span>} JSON オブジェクトとローカライゼーションデータ。 </p> <p>詳しくは、<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1" format="dita" scope="local"> ユーザーインターフェイス要素</a>のローカライズを参照してください。 </p> <p>オブジェクトの内容について詳しくは、<i>Viewer SDK ユーザーガイド </i>および例も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

[init](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)も参照してください。

## 返品 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"Video360Player.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played."},"fr":{"Video360Player.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus."},defaultLocale:"en"})
```
