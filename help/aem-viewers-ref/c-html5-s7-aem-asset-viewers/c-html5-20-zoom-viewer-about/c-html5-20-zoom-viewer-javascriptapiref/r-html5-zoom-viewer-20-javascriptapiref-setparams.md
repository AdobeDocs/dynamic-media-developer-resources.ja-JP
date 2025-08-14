---
title: setParams
description: ビデオビューア用のJavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: af31b5eb-2051-4f4c-861d-67ada3248fd6
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 2%

---

# setParams{#setparams}

ビデオビューア用のJavaScript API リファレンス。

` setParams( *`params`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph">{string} name=value パラメーターのペアを </span> &amp;<span class="codeph"> で区切って </span> 定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

1 つ以上のパラメーターを指定された値に設定します。 メソッド引数の構文は、URL クエリ文字列と同じです。 つまり、名前=値のペアを `&` で区切って表します。 クエリ文字列の場合と同様に、名前と値は UTF8 を使用してパーセント エンコードされます。 を呼び出す前に、このパラメーター `init()` 呼び出す必要があります。

ビューア設定情報が JSON オブジェクトとともにコンストラクターに渡された場合 `config` このメソッドはオプションです。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b) も参照してください。

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("ZoomView.zoomfactor=2,3&ZoomView.iscommand=op_sharpen%3d1")
```
