---
description: カルーセルビューアのJavaScript APIリファレンス。
solution: Experience Manager
title: setParams
feature: Dynamic Mediaクラシック，ビューア，SDK/API，カルーセルバナー
role: 開発者、業務従事者
exl-id: 4bf3f8f8-73fe-4ab1-8005-aa49e4ffaba6
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 2%

---

# setParams{#setparams}

カルーセルビューアのJavaScript APIリファレンス。

` setParams( *`params`*)`

1つ以上のパラメーターに特定の値を設定します。 メソッド引数の構文は、URLクエリ文字列と同じです。 つまり、name=valueのペアを`&`で区切って表します。 クエリ文字列と同様に、名前と値はUTF8を使用してパーセントでエンコードします。 `init()`を呼び出す前に、このパラメーターを呼び出す必要があります。

ビューアの設定情報が`config` JSONオブジェクトを使用して渡された場合は、このメソッドはオプションです。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)も参照してください。

## パラメータ {#section-add05f3d7ca0426897bd74bf7ac9b9cd}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=valueパラメーターのペアを <span class="codeph"> &amp;で区切ります</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101}を返す

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("CarouselView.fmt=png&CarouselView.iscommand=op_sharpen%3d1")
```
