---
title: setAsset
description: インラインズームビューアの JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 62b46ad5-90b7-49e1-a426-87fbe956f07e
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 2%

---

# setAsset{#setasset}

インラインズームビューアの JavaScript API リファレンス。

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> アセット</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> 文字列</span>} 新しいアセット ID、明示的な画像セット、またはフレーム固有の画像サービング修飾子を含む明示的な画像セット。オプションのグローバル画像サービング修飾子を後に付加します。 <span class="codeph"> ?</span>. </p> <p> IR（画像レンダリング）または UGC（ユーザー生成コンテンツ）を使用する画像は、このビューアではサポートされません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

新しいアセットを設定します。 このパラメーターは、いつでも（前後に）呼び出すことができます `init()`. 次の後に呼び出された場合 `init()`を指定した場合、ビューアは実行時にアセットをスワップします。

関連トピック [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463).

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

単一の画像参照：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

カタログで定義されている画像セットへの単一の参照：

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

セット内のすべての画像にシャープ修飾子が追加されました。

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C?op_sharpen=1")
```
