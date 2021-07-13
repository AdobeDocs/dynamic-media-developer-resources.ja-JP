---
description: スピンビューアのJavaScript APIリファレンス。
solution: Experience Manager
title: setParam
feature: Dynamic Media Classic，ビューア，SDK/API，スピンセット
role: Developer,User
exl-id: 16d1d2cd-f58f-4ac3-b89f-f2f12fee231d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 2%

---

# setParam{#setparam}

スピンビューアのJavaScript APIリファレンス。

` setParam( *`名前、値`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> name  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}パラメ </span> ーターの名前。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}パラメ </span> ーターの値。値をパーセントでエンコードすることはできません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ビューアのパラメータを指定した値に設定します。 パラメータは、ビューア固有の設定オプションまたはソフトウェア開発キット修飾子です。 このパラメータは`init()`の前に呼び出されます。

ビューアの設定情報が`config` JSONオブジェクトを使用して渡される場合は、このメソッドはオプションです。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae)も参照してください。

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```
