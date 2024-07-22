---
title: setAsset
description: ビデオビューア用のJavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 04b6bf4d-5c42-49e9-b585-de75ebf6c89f
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 1%

---

# setAsset{#setasset}

ビデオビューア用のJavaScript API リファレンス。

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> asset </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> String </span>} 新しいアセット ID またはオプションの画像サービング修飾子が <span class="codeph">？の後に追加された明示的な画像セット</span>。 </p> <p> IR （画像レンダリング）または UGC （ユーザー生成コンテンツ）を使用する画像は、このビューアではサポートされていません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

新しいアセットを設定します。 このパラメーターは、`init()` の前または後であればいつでも呼び出すことができます。 `init()` 後に呼び出された場合、ビューアは実行時にアセットをスワップします。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b) も参照してください。

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

カタログで定義される画像セットへの単一の参照：

```
 <instance>.setAsset("Viewers/Pluralist")
```

事前組み合わせページを使用した明示的画像セット：

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C,Scene7SharedAssets/Backpack_H,Scene7SharedAssets/Backpack_J")
```

個々のページ画像を含む明示的画像セット：

```
 <instance>.setAsset("Scene7SharedAssets/AdobeScene7_Overview_US-1,Scene7SharedAssets/AdobeScene7_Overview_US-2:AdobeScene7_Overview_US-3,Scene7SharedAssets/AdobeScene7_Overview_US-4")
```

セット内のすべての画像に追加されたシャープニング修飾子：

```
 <instance>.setAsset("Viewers/Pluralist?op_sharpen=1")
```
