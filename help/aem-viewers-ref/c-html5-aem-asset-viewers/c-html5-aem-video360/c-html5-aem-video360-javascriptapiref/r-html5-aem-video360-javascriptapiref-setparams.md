---
title: setParams
description: Video360 ビューアの JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 3c228b84-fbad-434f-96b4-d52485711844
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 3%

---

# setParams{#setparams}

Video360 ビューアの JavaScript API リファレンス。

` setParams( *`params`*)`

1 つ以上のパラメータを指定した値に設定します。 メソッド引数の構文は、URL クエリ文字列と同じです。 つまり、name=value のペアを `&` で区切って表します。 クエリ文字列と同様に、名前と値は UTF8 を使用してパーセントでエンコードされます。 `init()` を呼び出す前に、このパラメータを呼び出す必要があります。

ビューアの設定情報が `config` JSON オブジェクトを使用して渡された場合は、このメソッドはオプションです。

[init](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b) も参照してください。

## パラメータ {#section-add05f3d7ca0426897bd74bf7ac9b9cd}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span>  name=value パラメーターのペアを&amp;で区切 <span class="codeph"> ります</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("style=customStyle.css&VideoPlayer.playback=progressive")
```
