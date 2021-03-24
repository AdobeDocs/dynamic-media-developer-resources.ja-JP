---
description: 基本ズームビューアのJavaScript APIリファレンス。
solution: Experience Manager
title: setAsset
feature: Dynamic Mediaクラシック，ビューア，SDK/API，ズーム
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 3%

---


# setAsset{#setasset}

基本ズームビューアのJavaScript APIリファレンス。

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> asset</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>}新しいアセットID。オプションとして「?」の後にIS修飾子を付加できます。 </p> <p> IR（画像レンダリング）またはUGC（ユーザ生成コンテンツ）を使用する画像は、このビューアではサポートされていません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

新しいアセットを設定します。 このパラメーターは、`init()`の前後いつでも呼び出すことができます。 `init()`の後に呼び出した場合、ビューアは実行時にアセットを入れ替えます。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)も参照してください。

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101}を返す

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

1つの画像参照：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

セット内のすべての画像にシャープ修飾子を追加：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B?op_sharpen=1")
```

