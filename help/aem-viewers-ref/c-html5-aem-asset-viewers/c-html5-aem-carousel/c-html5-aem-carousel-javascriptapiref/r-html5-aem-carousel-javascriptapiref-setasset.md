---
description: カルーセルビューアのJavaScript APIリファレンス。
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic，ビューア，SDK/API，カルーセルバナー
role: Developer,Business Practitioner
exl-id: e8aaee4e-56d5-46e4-8499-d5c9a6ba5d3b
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 3%

---

# setAsset{#setasset}

カルーセルビューアのJavaScript APIリファレンス。

` setAsset( *`asset`*)`

新しいアセットを設定します。 このパラメーターは、`init()`の前後にいつでも呼び出すことができます。 `init()`の後に呼び出した場合、ビューアは実行時にアセットを入れ替えます。

[init](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)も参照してください。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> アセット</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>}新しいアセットID。 </p> <p>IR（画像レンダリング）またはUGC（ユーザー生成コンテンツ）を使用する画像は、このビューアではサポートされていません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

単一の画像参照：

```
<instance>.setAsset("/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner")
```
