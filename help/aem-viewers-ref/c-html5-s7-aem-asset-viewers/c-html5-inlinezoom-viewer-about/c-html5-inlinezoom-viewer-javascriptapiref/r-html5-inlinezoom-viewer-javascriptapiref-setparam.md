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

---


# setParam{#setparam}

インラインズームビューアのJavaScript APIリファレンス。

` setParam( *`名前、値`*)`

ビューアのパラメータを指定した値に設定します。 このパラメータは、ビューア固有の設定オプションまたはソフトウェア開発キット修飾子のいずれかです。 このパラメーターは、前に呼び出されま `init()`す。 ビューアの設定情報が `config` JSONオブジェクトを使用して渡される場合、このメソッドはオプションです。

「 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463)」も参照。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 名 </span> 前 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}パラメ </span> ーターの名前。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 価 </span> 値 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}パラメ </span> ーターの値。 値をパーセントでエンコードすることはできません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```

