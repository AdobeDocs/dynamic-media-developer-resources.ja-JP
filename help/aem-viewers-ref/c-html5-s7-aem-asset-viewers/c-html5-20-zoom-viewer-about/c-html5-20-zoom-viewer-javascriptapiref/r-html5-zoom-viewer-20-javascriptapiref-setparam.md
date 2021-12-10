---
title: setParam
description: ビデオビューアの JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: d797a8be-582e-46f4-9068-db1d2757970d
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 2%

---

# setParam{#setparam}

ビデオビューアの JavaScript API リファレンス。

` setParam( *`名前、値`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 名前 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> パラメーターの名前。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 値 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> パラメーターの値。 値をパーセントでエンコードすることはできません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ビューアのパラメータを指定した値に設定します。 パラメータは、ビューア固有の設定オプションか、ソフトウェア開発キットの修飾子のどちらかです。 このパラメーターは、 `init()`.

ビューアの設定情報がで渡された場合は、このメソッドはオプションです。 `config` JSON オブジェクトをコンストラクターに渡します。

関連トピック [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```
