---
description: ビデオビューアのJavaScript APIリファレンス。
solution: Experience Manager
title: setParam
feature: Dynamic Media Classic，ビューア，SDK/API，ズーム
role: Developer,Business Practitioner
exl-id: d797a8be-582e-46f4-9068-db1d2757970d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 2%

---

# setParam{#setparam}

ビデオビューアのJavaScript APIリファレンス。

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

ビューアの設定情報が`config` JSONオブジェクトを使用して渡された場合は、このメソッドはオプションです。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)も参照してください。

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```
