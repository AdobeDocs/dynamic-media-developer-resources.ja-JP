---
title: setAsset
description: ビデオビューアの JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 04b6bf4d-5c42-49e9-b585-de75ebf6c89f
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 2%

---

# setAsset{#setasset}

ビデオビューアの JavaScript API リファレンス。

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> アセット </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> 文字列 </span>} オプションの画像サービング修飾子を後に付けた新しいアセット ID または明示的な画像セット <span class="codeph"> ? </span>. </p> <p> IR（画像レンダリング）または UGC（ユーザー生成コンテンツ）を使用する画像は、このビューアではサポートされません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

新しいアセットを設定します。 このパラメーターは、いつでも（前後に）呼び出すことができます `init()`. 次の後に呼び出された場合 `init()`を指定した場合、ビューアは実行時にアセットをスワップします。

関連トピック [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

カタログで定義されている画像セットへの単一の参照：

```
 <instance>.setAsset("Viewers/Pluralist")
```

明示的な画像セット（事前に結合されたページを含む）:

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C,Scene7SharedAssets/Backpack_H,Scene7SharedAssets/Backpack_J")
```

明示的な画像セット（個々のページ画像を含む）:

```
 <instance>.setAsset("Scene7SharedAssets/AdobeScene7_Overview_US-1,Scene7SharedAssets/AdobeScene7_Overview_US-2:AdobeScene7_Overview_US-3,Scene7SharedAssets/AdobeScene7_Overview_US-4")
```

セット内のすべての画像にシャープ修飾子が追加されました。

```
 <instance>.setAsset("Viewers/Pluralist?op_sharpen=1")
```
