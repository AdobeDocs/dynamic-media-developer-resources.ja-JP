---
title: setAsset
description: ビデオビューア用のJavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 4fc94f30-e330-4c8a-b6da-d870e4f8e4ab
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 1%

---

# setAsset{#setasset}

ビデオビューア用のJavaScript API リファレンス。

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> asset </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> String </span>} 新しいアセット ID、明示的な画像セット、またはフレーム固有の画像サービング修飾子を持つ明示的な画像セット。オプションのグローバル画像サービング修飾子が「?」の後に追加されます。 </p> <p> IR （画像レンダリング）または UGC （ユーザー生成コンテンツ）を使用する画像は、このビューアではサポートされていません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

新しいアセットを設定します。 このパラメーターは、`init()` の前または後であればいつでも呼び出すことができます。 `init()` 後に呼び出された場合、ビューアは実行時にアセットをスワップします。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b) も参照してください。

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

単一の画像参照を次に示します。

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

カタログ内で次のように定義される画像セットへの単一の参照。

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample")
```

明示的な画像は次のように設定されます。

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

フレーム固有の画像サービング修飾子を持つ明示的な画像セットを次に示します。

```
 <instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

セット内のすべての画像に追加されたシャープニング修飾子を次に示します。

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample?op_sharpen=1")
```
