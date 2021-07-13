---
description: 基本ズームビューアのJavaScript APIリファレンス。
solution: Experience Manager
title: setParams
feature: Dynamic Media Classic，ビューア，SDK/API，ズーム
role: Developer,User
exl-id: f142dd72-5e45-44f6-a79b-3eaf6a310bde
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 1%

---

# setParams{#setparams}

基本ズームビューアのJavaScript APIリファレンス。

` setParams( *`params`*)`

1つ以上のパラメーターに指定した値を設定します。 メソッド引数の構文は、URLクエリ文字列と同じです。 つまり、name=valueのペアを`&`で区切って表します。 クエリ文字列と同様に、名前と値はUTF8を使用してパーセントでエンコードされます。 `init()`を呼び出す前に、このパラメーターを呼び出す必要があります。

ビューアの設定情報が`config` JSONオブジェクトを使用して渡された場合は、このメソッドはオプションです。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)も参照してください。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=valueパラメーターのペアを&amp;で区 <span class="codeph"> 切ります</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("ZoomView.zoomfactor=2,3&ZoomView.iscommand=op_sharpen%3d1")
```
