---
title: setParam
description: ビデオビューアの JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: b28ffb51-1091-4f2e-b12d-904218daf117
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 2%

---

# setParam{#setparam}

ビデオビューアの JavaScript API リファレンス。

` setParam( *`名前、値`*)`

ビューアのパラメータを指定した値に設定します。 パラメータは、ビューア固有の設定オプションか、ソフトウェア開発キットの修飾子のどちらかです。 このパラメーターは、 `init()`.

ビューアの設定情報がで渡された場合は、このメソッドはオプションです。 `config` JSON オブジェクトをコンストラクターに追加します。

関連トピック [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

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
