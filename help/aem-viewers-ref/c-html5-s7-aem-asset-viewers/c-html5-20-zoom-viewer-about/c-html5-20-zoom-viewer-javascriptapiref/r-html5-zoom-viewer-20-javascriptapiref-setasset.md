---
title: setAsset
description: ビデオビューアの JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 4fc94f30-e330-4c8a-b6da-d870e4f8e4ab
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 2%

---

# setAsset{#setasset}

ビデオビューアの JavaScript API リファレンス。

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> アセット </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> 文字列 </span>} 新しいアセット id、明示的な画像セット、またはフレーム固有の画像サービング修飾子を含む明示的な画像セット。オプションとして「?」の後にグローバルな画像サービング修飾子を追加できます。 </p> <p> IR（画像レンダリング）または UGC（ユーザー生成コンテンツ）を使用する画像は、このビューアではサポートされません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

新しいアセットを設定します。 このパラメーターは、いつでも（前後に）呼び出すことができます `init()`. 次の後に呼び出された場合 `init()`を指定した場合、ビューアは実行時にアセットをスワップします。

関連トピック [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

次に示す単一の画像参照：

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

次のようにカタログ内で定義された画像セットへの 1 つの参照。

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample")
```

明示的な画像セットを次に示します。

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

次に示す、フレーム固有の画像サービング修飾子を含む明示的な画像セット：

```
 <instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

セット内のすべての画像に追加されたシャープ修飾子：

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample?op_sharpen=1")
```
