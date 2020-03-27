---
description: 混在メディアビューアのJavaScript APIリファレンス。
seo-description: 混在メディアビューアのJavaScript APIリファレンス。
seo-title: setParam
solution: Experience Manager
title: setParam
topic: Dynamic media
uuid: 427daeae-f7b4-4eb0-a285-e5b16c538239
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setParam{#setparam}

混在メディアビューアのJavaScript APIリファレンス。

` setParam( *`名前、値`*)`

ビューアのパラメータを指定した値に設定します。 このパラメータは、ビューア固有の設定オプションまたはソフトウェア開発キット修飾子のいずれかです。 このパラメーターは、前に呼び出されま `init()`す。 ビューアの設定情報が `config` JSONオブジェクトを使用して渡される場合、このメソッドはオプションです。

「 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae)」も参照。

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

