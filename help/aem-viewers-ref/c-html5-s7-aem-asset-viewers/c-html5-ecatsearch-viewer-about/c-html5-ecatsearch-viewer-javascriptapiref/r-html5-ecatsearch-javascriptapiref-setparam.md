---
description: eCatalogビューアのJavaScript APIリファレンス。
solution: Experience Manager
title: setParam
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog検索
role: Developer,User
exl-id: 0dd57c7e-c20f-4e8f-a872-42e24305fc0c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 2%

---

# setParam{#setparam}

eCatalogビューアのJavaScript APIリファレンス。

[!DNL ` setParam( *`名前、値`*)`]

ビューアのパラメータを指定した値に設定します。 パラメータは、ビューア固有の設定オプションまたはソフトウェア開発キット修飾子です。 このパラメータは[!DNL `init()`]の前に呼び出されます。

ビューアの設定情報が[!DNL `config`] JSONオブジェクトを使用して渡される場合は、このメソッドはオプションです。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)も参照してください。

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

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
[!DNL <instance>.setParam("style", "customStyle.css")]
```
