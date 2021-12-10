---
title: setParams
description: ビデオビューアの JavaScript API リファレンス。
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

ビデオビューアの JavaScript API リファレンス。

` setParams( *`params`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value パラメーターのペアを区切って指定します。 <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

1 つ以上のパラメータを指定された値に設定します。 メソッド引数の構文は、URL クエリ文字列と同じです。 つまり、name=value のペアを `&`. クエリ文字列と同様に、名前と値は UTF8 を使用してパーセントでエンコードされます。 電話する前に `init()`に設定する場合は、このパラメーターを呼び出す必要があります。

ビューアの設定情報がで渡された場合は、このメソッドはオプションです。 `config` JSON オブジェクトをコンストラクターに渡します。

関連トピック [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("ZoomView.zoomfactor=2,3&ZoomView.iscommand=op_sharpen%3d1")
```
