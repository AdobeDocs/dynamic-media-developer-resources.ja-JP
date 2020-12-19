---
description: インラインズームビューアのJavaScript APIリファレンス。
seo-description: インラインズームビューアのJavaScript APIリファレンス。
seo-title: setParam
solution: Experience Manager
title: setParam
topic: Dynamic media
uuid: 7bccf2c0-9f9a-47ac-8b53-385989e8267c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 2%

---


# setParam{#setparam}

インラインズームビューアのJavaScript APIリファレンス。

` setParam( *`name、value`*)`

ビューアのパラメータを指定した値に設定します。 パラメータは、ビューア固有の設定オプションか、ソフトウェア開発キットの修飾子のいずれかです。 このパラメーターは`init()`の前に呼び出されます。 ビューアの設定情報が`config` JSONオブジェクトを使用して渡される場合は、このメソッドはオプションです。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463)も参照してください。

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

