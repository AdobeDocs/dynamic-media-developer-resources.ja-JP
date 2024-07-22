---
description: eCatalog ビューアのJavaScript API リファレンス。
solution: Experience Manager
title: setParam
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 0dd57c7e-c20f-4e8f-a872-42e24305fc0c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 2%

---

# setParam{#setparam}

eCatalog ビューアのJavaScript API リファレンス。

[!DNL ` setParam( *` 名前、値 `*)`]

ビューアパラメーターを指定した値に設定します。 パラメーターは、ビューア固有の設定オプションか、ソフトウェア開発キットの修飾子です。 このパラメーターは、[!DNL `init()`] 前に呼び出されます。

ビューアの設定情報が JSON オブジェクトとともにコンストラクターに渡され [!DNL `config`] 場合、このメソッドはオプションです。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b) も参照してください。

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
[!DNL <instance>.setParam("style", "customStyle.css")]
```
