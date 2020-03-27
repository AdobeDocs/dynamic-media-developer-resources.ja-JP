---
description: ビデオ画像ビューアのJavaScript APIリファレンス。
seo-description: ビデオ画像ビューアのJavaScript APIリファレンス。
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: 8cb10b2e-addb-4659-a93b-5a53d0f8a5bb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAsset{#setasset}

ビデオ画像ビューアのJavaScript APIリファレンス。

` setAsset( *`asset`*)`

新しいアセットを設定します。 このパラメーターは、いつでも、前でも後でも呼び出すことができま `init()`す。 後に呼び出した場合、ビュ `init()`ーアは実行時にアセットを入れ替えます。

「 [init](../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-javascriptapiref/r-html5-aem-int-image-viewer-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)」も参照。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 資 <span class="varname"> 産</span></span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>}新しいアセットID。 </p> <p>IR（画像レンダリング）またはUGC（ユーザ生成コンテンツ）を使用する画像は、このビューアではサポートされていません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

1つの画像参照：

```
<instance>.setAsset("/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg")
```

