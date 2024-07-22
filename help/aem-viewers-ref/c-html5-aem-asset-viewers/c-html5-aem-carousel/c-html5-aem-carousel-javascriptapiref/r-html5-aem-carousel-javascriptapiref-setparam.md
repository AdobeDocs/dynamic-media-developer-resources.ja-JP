---
title: setParam
description: カルーセルビューアのJavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 0829933f-a90b-4066-9904-748f2a727169
source-git-commit: 96ac67e5645c2c55920cc971806ba2f14ae57044
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 2%

---

# setParam{#setparam}

カルーセルビューアのJavaScript API リファレンス。

` setParam( *` 名前、値 `*)`

ビューアパラメーターを指定した値に設定します。 パラメーターは、ビューア固有の設定オプションか、ソフトウェア開発キットの修飾子です。 このパラメーターは、`init()` 前に呼び出されます。

ビューア設定情報が JSON オブジェクトとともにコンストラクターに渡された場合 `config` このメソッドはオプションです。

[xref](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md) も参照してください。

## パラメーター {#section-c68a5a3688d342fd9d6a7fd59867cc7a}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> の名前 </span> </span> </p> </td>
   <td colname="col2"> <p> <span class="codeph"> {string} パラメーター </span> 名前。 </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 値 </span> </span> </p> </td>
   <td colname="col2"> <p> <span class="codeph"> {string} パラメーターの </span> 値。 値はパーセント エンコードできません。 </p> </td>
  </tr>
 </tbody>
</table>

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "etc/dam/presets/css/html5_carouselviewer_dotted_light.css")
```
