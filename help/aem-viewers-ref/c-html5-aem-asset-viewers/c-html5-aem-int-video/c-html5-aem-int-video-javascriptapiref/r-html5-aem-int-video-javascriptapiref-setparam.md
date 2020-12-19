---
description: インタラクティブビデオビューアのJavaScript APIリファレンス。
seo-description: インタラクティブビデオビューアのJavaScript APIリファレンス。
seo-title: setParam
solution: Experience Manager
title: setParam
topic: Dynamic media
uuid: c8c40e88-530f-4af8-be9a-2e88addd6907
translation-type: tm+mt
source-git-commit: 94b8dde58cda2670f3e2f22f217599c23601e450
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 3%

---


# setParam{#setparam}

インタラクティブビデオビューアのJavaScript APIリファレンス。

` setParam( *`name、value`*)`

ビューアのパラメータを指定した値に設定します。 パラメータは、ビューア固有の設定オプションか、ソフトウェア開発キットの修飾子のいずれかです。 このパラメーターは`init()`の前に呼び出されます。

ビューアの設定情報が`config` JSONオブジェクトを使用して渡された場合は、このメソッドはオプションです。

[init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)も参照してください。

## パラメータ {#section-c68a5a3688d342fd9d6a7fd59867cc7a}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> name  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}パラメーターの </span> 名前。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}パラメーターの </span> 値。値をパーセントでエンコードすることはできません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101}を返す

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```

