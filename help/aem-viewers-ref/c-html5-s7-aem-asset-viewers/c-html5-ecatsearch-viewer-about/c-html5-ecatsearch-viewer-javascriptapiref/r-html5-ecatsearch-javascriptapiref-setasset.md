---
description: ビデオビューアのJavaScript APIリファレンス。
seo-description: ビデオビューアのJavaScript APIリファレンス。
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: ab078f32-c523-4b6c-a0d6-45dd2af35b36
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 2%

---


# setAsset{#setasset}

ビデオビューアのJavaScript APIリファレンス。

[!DNL ` setAsset( *`asset`*)`]

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> asset  </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph">文字列</span>}新しいアセットIDまたは明示的な画像セット。オプションとして<span class="codeph">の後に画像サービング修飾子を付加できますか？</span>。 </p> <p> IR（画像レンダリング）またはUGC（ユーザ生成コンテンツ）を使用する画像は、このビューアではサポートされていません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

新しいアセットを設定します。 このパラメーターは、[!DNL `init()`]の前後いつでも呼び出すことができます。 [!DNL `init()`]の後に呼び出した場合、ビューアは実行時にアセットを入れ替えます。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)も参照してください。

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101}を返す

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

カタログに定義されている画像セットへの1つの参照：

```
 <instance>.setAsset("Viewers/Pluralist")
```

明示的な画像セット（事前に組み合わされたページを含む）:

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

