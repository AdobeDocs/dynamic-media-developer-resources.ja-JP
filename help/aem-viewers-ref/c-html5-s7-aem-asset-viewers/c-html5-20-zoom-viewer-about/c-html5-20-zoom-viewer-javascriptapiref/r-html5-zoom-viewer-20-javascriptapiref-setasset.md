---
description: ビデオビューアのJavaScript APIリファレンス。
seo-description: ビデオビューアのJavaScript APIリファレンス。
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic Media
uuid: f106b3d4-880e-4ba3-ae47-a005af5c0f1b
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 2%

---


# setAsset{#setasset}

ビデオビューアのJavaScript APIリファレンス。

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> asset  </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> String </span>}新しいアセットID、明示的な画像セット、またはフレーム固有の画像サービング修飾子を含む明示的な画像セット。オプションとして「?」の後にグローバルの画像サービング修飾子を付加できます。 </p> <p> IR（画像レンダリング）またはUGC（ユーザ生成コンテンツ）を使用する画像は、このビューアではサポートされていません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

新しいアセットを設定します。 このパラメーターは、`init()`の前後いつでも呼び出すことができます。 `init()`の後に呼び出した場合、ビューアは実行時にアセットを入れ替えます。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)も参照してください。

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101}を返す

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

1つの画像参照：

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

カタログに定義されている画像セットへの1つの参照：

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample")
```

明示的な画像セット：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

フレーム固有の画像サービング修飾子を含む明示的な画像セット：

```
 <instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

セット内のすべての画像にシャープ修飾子を追加：

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample?op_sharpen=1")
```

