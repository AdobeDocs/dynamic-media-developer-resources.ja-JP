---
title: setParams
description: インタラクティブビデオビューアのJavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 32d26999-7815-4c71-ad4c-b7db99ec3d3b
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 3%

---

# setParams{#setparams}

インタラクティブビデオビューアのJavaScript API リファレンス。

` setParams( *`params`*)`

1 つ以上のパラメーターを指定された値に設定します。 メソッド引数の構文は、URL クエリ文字列と同じです。 つまり、名前=値のペアを `&` で区切って表します。 クエリ文字列の場合と同様に、名前と値は UTF8 を使用してパーセント エンコードされます。 を呼び出す前に、このパラメーター `init()` 呼び出す必要があります。

ビューア設定情報が JSON オブジェクトとともにコンストラクターに渡された場合 `config` このメソッドはオプションです。

[init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b) も参照してください。


## パラメータ {#section-add05f3d7ca0426897bd74bf7ac9b9cd}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> {string}</span> name=value パラメーターのペアを <span class="codeph"> &amp;</span> で区切って <span class="codeph"> 定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("style=customStyle.css&VideoPlayer.playback=progressive")
```
