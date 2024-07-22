---
title: setParam
description: スピンビューアのJavaScript API リファレンスです。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 16d1d2cd-f58f-4ac3-b89f-f2f12fee231d
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 2%

---

# setParam{#setparam}

スピンビューアのJavaScript API リファレンスです。

` setParam( *` 名前、値 `*)`

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

ビューアパラメーターを指定した値に設定します。 パラメーターは、ビューア固有の設定オプションか、ソフトウェア開発キットの修飾子です。 このパラメーターは、`init()` 前に呼び出されます。

ビューアの設定情報が JSON オブジェクトとともにコンストラクターに渡され `config` 場合、このメソッドはオプションです。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae) も参照してください。

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```
