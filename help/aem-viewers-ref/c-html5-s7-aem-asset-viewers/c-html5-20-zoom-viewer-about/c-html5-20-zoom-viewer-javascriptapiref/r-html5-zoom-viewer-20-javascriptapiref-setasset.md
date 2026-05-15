---
title: setAsset
description: ビデオビューア用JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 4fc94f30-e330-4c8a-b6da-d870e4f8e4ab
TQID: 'https://experienceleague.adobe.com/WSUZln6WtAUoNCL-BsnmGg9PKJw-8T5ozloMvzTyzuo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 138
ht-degree: 1%

---

# setAsset{#setasset}

ビデオビューア用JavaScript API リファレンス。

` setAsset( *` アセット `*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> アセット </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph">文字列</span>}新しいアセット ID、明示的な画像セット、またはフレーム固有の画像サービング修飾子を使用した明示的な画像セット。オプションのグローバル画像サービング修飾子は「?」の後に追加されます。 </p> <p> IR （画像レンダリング）またはUGC （ユーザー生成コンテンツ）を使用する画像は、このビューアではサポートされていません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

新しいアセットを設定します。 このパラメーターは、`init()`の前または後に、いつでも呼び出すことができます。 `init()`の後に呼び出された場合、ビューアは実行時にアセットを入れ替えます。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)も参照してください。

## 返品 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

単一の画像参照を次のように指定します。

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

カタログで次のように定義されている画像セットへの単一参照：

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample")
```

次のように明示的な画像セット：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

フレーム固有の画像サービング修飾子を使用した明示的な画像セットは次のとおりです。

```
 <instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

シャープ修飾子は、次のようにセット内のすべての画像に追加されました。

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample?op_sharpen=1")
```
