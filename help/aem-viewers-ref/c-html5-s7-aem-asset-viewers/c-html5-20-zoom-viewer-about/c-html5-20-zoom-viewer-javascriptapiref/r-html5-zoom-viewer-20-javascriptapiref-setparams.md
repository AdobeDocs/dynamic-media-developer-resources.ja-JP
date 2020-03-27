---
description: ビデオビューアのJavaScript APIリファレンス。
seo-description: ビデオビューアのJavaScript APIリファレンス。
seo-title: setParams
solution: Experience Manager
title: setParams
topic: Dynamic media
uuid: 2f431747-df81-49ed-b323-c70080883c8a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setParams{#setparams}

ビデオビューアのJavaScript APIリファレンス。

` setParams( *`params`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=valueパラメーターのペアを <span class="codeph"> &amp;で区切</span>る。 </p> </td> 
  </tr> 
 </tbody> 
</table>

1つ以上のパラメーターを指定された値に設定します。 メソッドの引数の構文は、URLクエリ文字列と同じです。 つまり、name=valueのペアをで区切って表します `&`。 クエリ文字列と同様に、名前と値はUTF8を使用してパーセントでエンコードされます。 を呼び出す前に、こ `init()`のパラメーターを呼び出す必要があります。

ビューアの設定情報が `config` JSONオブジェクトと共に渡された場合、このメソッドはオプションです。

「 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)」も参照。

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("ZoomView.zoomfactor=2,3&ZoomView.iscommand=op_sharpen%3d1")
```

