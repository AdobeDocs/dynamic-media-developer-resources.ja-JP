---
title: setParam
description: 混在メディアビューア用のJavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 610a5a7d-1314-48bc-a640-319139d64adc
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 2%

---

# setParam{#setparam}

混在メディアビューア用のJavaScript API リファレンス。

` setParam( *` 名前、値 `*)`

ビューアパラメーターを指定した値に設定します。 パラメーターは、ビューア固有の設定オプションか、ソフトウェア開発キットの修飾子です。 このパラメーターは、`init()` 前に呼び出されます。 ビューアの設定情報が JSON オブジェクトと共にコンストラクターに渡され `config` 場合、このメソッドはオプションです。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae) も参照してください。

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
<instance>.setParam("style", "customStyle.css")
```
