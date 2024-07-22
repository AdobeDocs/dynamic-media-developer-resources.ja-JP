---
title: setParams
description: Flyout ビューアのJavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: bd26292d-f9c6-4e67-8cc1-c74336d50860
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 2%

---

# setParams{#setparams}

Flyout ビューアのJavaScript API リファレンス。

` setParams( *`params`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> {string}</span> name=value パラメーターのペアを <span class="codeph"> &amp;</span> で区切って <span class="codeph"> 定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

1 つ以上のパラメーターを指定された値に設定します。 メソッド引数の構文は、URL クエリ文字列と同じです。 つまり、名前=値のペアを `&` で区切って表します。 クエリ文字列の場合と同じように、名前と値は UTF8 を使用してパーセント エンコードされます。 を呼び出す前に、このパラメーター `init()` 呼び出す必要があります。 ビューアの設定情報が JSON オブジェクトと共にコンストラクターに渡され `config` 場合、このメソッドはオプションです。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463) も参照してください。

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("FlyoutZoomView.zoomfactor=2,3&Swatches.iscommand=op_sharpen%3d1")
```
