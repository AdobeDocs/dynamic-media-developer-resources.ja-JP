---
title: setParam
description: ビデオビューア用JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: d797a8be-582e-46f4-9068-db1d2757970d
TQID: 'https://experienceleague.adobe.com/qMJpaoYBwrt7LXiAluW-ay43OvYCyTfT7ZALpa7HenM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 82
ht-degree: 2%

---

# setParam{#setparam}

ビデオビューア用JavaScript API リファレンス。

` setParam( *`name, value`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">名</span> </span> </p> </td> 
   <td colname="col2"> <p> パラメーターの<span class="codeph"> {string} </span>名。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">値</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> パラメーターの値。 値をパーセント エンコードすることはできません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ビューアパラメーターを指定した値に設定します。 パラメーターは、ビューア固有の設定オプションまたはソフトウェア開発キット修飾子です。 このパラメーターは`init()`の前に呼び出されます。

ビューア設定情報が`config` JSON オブジェクトでコンストラクターに渡された場合、このメソッドはオプションです。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)も参照してください。

## 返品 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```

