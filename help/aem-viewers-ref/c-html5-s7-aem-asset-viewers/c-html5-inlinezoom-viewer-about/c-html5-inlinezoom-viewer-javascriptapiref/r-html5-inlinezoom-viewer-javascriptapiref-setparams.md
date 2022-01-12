---
title: setParams
description: インラインズームビューアの JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: eb3298da-f19d-4013-8192-c51144d8b866
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 2%

---

# setParams{#setparams}

インラインズームビューアの JavaScript API リファレンス。

` setParams( *`params`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value パラメーターのペアを区切って指定します。 <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

1 つ以上のパラメータを指定された値に設定します。 メソッド引数の構文は、URL クエリ文字列と同じです。 つまり、name=value のペアを `&`. クエリ文字列と同様に、名前と値は UTF8 を使用してパーセントでエンコードされます。 電話する前に `init()`に設定する場合は、このパラメーターを呼び出す必要があります。 ビューアの設定情報が `config` JSON オブジェクトをコンストラクターに追加します。

関連トピック [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463).

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("FlyoutZoomView.zoomfactor=2,3&Swatches.iscommand=op_sharpen%3d1")
```
