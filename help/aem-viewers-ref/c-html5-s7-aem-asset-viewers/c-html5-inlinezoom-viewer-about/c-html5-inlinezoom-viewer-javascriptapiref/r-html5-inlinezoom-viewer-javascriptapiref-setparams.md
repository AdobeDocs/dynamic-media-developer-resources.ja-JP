---
description: インラインズームビューアのJavaScript APIリファレンス。
solution: Experience Manager
title: setParams
feature: Dynamic Mediaクラシック，ビューア，SDK/API，インラインズーム
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 1%

---


# setParams{#setparams}

インラインズームビューアのJavaScript APIリファレンス。

` setParams( *`params`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=valueパラメーターのペアを <span class="codeph"> &amp;で区切ります</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

1つ以上のパラメーターに特定の値を設定します。 メソッド引数の構文は、URLクエリ文字列と同じです。 つまり、name=valueのペアを`&`で区切って表します。 クエリ文字列と同様に、名前と値はUTF8を使用してパーセントでエンコードします。 `init()`を呼び出す前に、このパラメーターを呼び出す必要があります。 ビューアの設定情報が`config` JSONオブジェクトを使用して渡される場合は、このメソッドはオプションです。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463)も参照してください。

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101}を返す

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("FlyoutZoomView.zoomfactor=2,3&Swatches.iscommand=op_sharpen%3d1")
```

