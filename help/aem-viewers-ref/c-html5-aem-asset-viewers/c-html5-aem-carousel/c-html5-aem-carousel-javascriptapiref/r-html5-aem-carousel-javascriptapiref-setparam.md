---
description: カルーセルビューアのJavaScript APIリファレンス。
solution: Experience Manager
title: setParam
feature: Dynamic Media Classic，ビューア，SDK/API，カルーセルバナー
role: Developer,User
exl-id: 0829933f-a90b-4066-9904-748f2a727169
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 3%

---

# setParam{#setparam}

カルーセルビューアのJavaScript APIリファレンス。

` setParam( *`名前、値`*)`

ビューアのパラメータを指定した値に設定します。 パラメータは、ビューア固有の設定オプションまたはソフトウェア開発キット修飾子です。 このパラメータは`init()`の前に呼び出されます。

ビューアの設定情報が`config` JSONオブジェクトを使用して渡された場合は、このメソッドはオプションです。

[外部参照](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md)も参照してください。

## パラメータ {#section-c68a5a3688d342fd9d6a7fd59867cc7a}

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
<instance>.setParam("style", "etc/dam/presets/css/html5_carouselviewer_dotted_light.css")
```
