---
description: スマート切り抜きビデオビューアの JavaScript API リファレンス。
solution: Experience Manager
title: setParams
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 76bad894-bfb8-4d79-b3ff-c2497c68e5e8
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 1%

---

# setParams{#setparams}

スマート切り抜きビデオビューアの JavaScript API リファレンス。

` setParams( *`params`*)`

1 つ以上のパラメータを指定された値に設定します。 メソッド引数の構文は、URL クエリ文字列と同じです。 つまり、name=value のペアを `&`. クエリ文字列と同様に、名前と値は UTF8 を使用してパーセントでエンコードされます。 電話する前に `init()`を指定する場合は、このパラメーターを呼び出す必要があります。

ビューアの設定情報が `config` JSON オブジェクトをコンストラクターに追加します。

関連トピック [init](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value パラメーターのペアを区切って指定します。 <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("style=customStyle.css&SmartCropVideoPlayer.playback=progressive")
```
