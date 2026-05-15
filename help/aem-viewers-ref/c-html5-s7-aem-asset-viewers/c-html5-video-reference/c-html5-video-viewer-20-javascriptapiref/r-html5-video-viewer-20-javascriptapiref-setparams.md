---
title: setParams
description: ビデオビューア用JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 76bad894-bfb8-4d79-b3ff-c2497c68e5e8
TQID: 'https://experienceleague.adobe.com/2tiBygflfs1VEqg-FjUepzP14XYq4CwEMVyUhiI08Tw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 98
ht-degree: 2%

---

# setParams{#setparams}

ビデオビューア用JavaScript API リファレンス。

` setParams( *` パラメーター`*)`

指定された値に1つ以上のパラメーターを設定します。 メソッド引数の構文は、URL クエリ文字列と同じです。 つまり、`&`で区切られたname=value ペアを表します。 クエリ文字列と同じように、名前と値はUTF8を使用してパーセント エンコードされます。 `init()`を呼び出す前に、このパラメーターを呼び出す必要があります。

ビューア設定情報が`config` JSON オブジェクトでコンストラクターに渡される場合、このメソッドはオプションです。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)も参照してください。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> パラメーター</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value パラメーターのペアが<span class="codeph">および</span>で区切られています。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返品 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```css{.line-numbers}
<instance>.setParams("style=customStyle.css&VideoPlayer.playback=progressive")
```
