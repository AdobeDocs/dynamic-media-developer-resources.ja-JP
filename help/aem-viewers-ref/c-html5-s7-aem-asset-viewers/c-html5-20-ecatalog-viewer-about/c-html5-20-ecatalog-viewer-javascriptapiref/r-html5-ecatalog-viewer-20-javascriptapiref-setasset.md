---
description: ビデオビューアのJavaScript APIリファレンス。
seo-description: ビデオビューアのJavaScript APIリファレンス。
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: b95cef30-41ad-47d5-b0f1-efc8831c7bdc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAsset{#setasset}

ビデオビューアのJavaScript APIリファレンス。

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 資 </span> 産 </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> String </span>}新しいアセットIDまたは明示的な画像セット。オプションとして「 <span class="codeph"> ?」の後に画像サービング修飾子を付加できます。 </span>. </p> <p> IR（画像レンダリング）またはUGC（ユーザ生成コンテンツ）を使用する画像は、このビューアではサポートされていません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

新しいアセットを設定します。 このパラメーターは、いつでも、前でも後でも呼び出すことができま `init()`す。 後に呼び出した場合、ビュ `init()`ーアは実行時にアセットを入れ替えます。

「 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)」も参照。

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

カタログ内で定義された画像セットへの1つの参照：

```
 <instance>.setAsset("Viewers/Pluralist")
```

明示的な画像セット、事前に組み合わされたページ：

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C,Scene7SharedAssets/Backpack_H,Scene7SharedAssets/Backpack_J")
```

明示的な画像セット（個別のページ画像を含む）:

```
 <instance>.setAsset("Scene7SharedAssets/AdobeScene7_Overview_US-1,Scene7SharedAssets/AdobeScene7_Overview_US-2:AdobeScene7_Overview_US-3,Scene7SharedAssets/AdobeScene7_Overview_US-4")
```

セット内のすべての画像にシャープ修飾子を追加：

```
 <instance>.setAsset("Viewers/Pluralist?op_sharpen=1")
```

