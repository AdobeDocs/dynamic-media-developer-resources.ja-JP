---
title: setAsset
description: Flyout ビューアのJavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: cd66267e-7b25-4af4-b83c-f7b7f768ea8c
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 1%

---

# setAsset{#setasset}

Flyout ビューアのJavaScript API リファレンス。

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> asset</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} 新しいアセット ID、フレーム固有の画像サービング修飾子を持つ明示的な画像セットまたは明示的な画像セット。オプションのグローバル画像サービング修飾子が <span class="codeph">?</span> の後に追加されます。 </p> <p> IR （画像レンダリング）または UGC （ユーザー生成コンテンツ）を使用する画像は、このビューアではサポートされていません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

新しいアセットを設定します。 このパラメーターは、`init()` の前または後であればいつでも呼び出すことができます。 `init()` 後に呼び出された場合、ビューアは実行時にアセットをスワップします。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463) も参照してください。

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

単一の画像参照：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

カタログで定義される画像セットへの単一の参照：

```
<instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample")
```

明示的な画像は次のように設定されます。

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

フレーム固有の画像サービング修飾子を持つ明示的な画像セット：

```
<instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

セット内のすべての画像に追加されたシャープニング修飾子：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C?op_sharpen=1")
```
