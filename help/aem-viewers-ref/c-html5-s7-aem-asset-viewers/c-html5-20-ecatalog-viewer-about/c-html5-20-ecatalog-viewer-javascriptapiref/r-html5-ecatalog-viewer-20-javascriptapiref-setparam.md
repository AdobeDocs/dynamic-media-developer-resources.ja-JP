---
title: setParam
description: eCatalog ビューアの JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 781982f6-488d-452c-8168-604c708ae6ce
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 2%

---

# setParam{#setparam}

eCatalog ビューアの JavaScript API リファレンス。

` setParam( *`名前、値`*)`

ビューアのパラメータを指定した値に設定します。 パラメータは、ビューア固有の設定オプションか、ソフトウェア開発キットの修飾子のどちらかです。 このパラメーターは、 `init()`.

ビューアの設定情報が `config` JSON オブジェクトをコンストラクターに追加します。

関連トピック [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

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

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```
