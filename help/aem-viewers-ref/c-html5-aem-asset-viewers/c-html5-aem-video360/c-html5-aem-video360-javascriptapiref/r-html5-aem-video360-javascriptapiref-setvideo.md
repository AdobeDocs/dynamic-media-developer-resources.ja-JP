---
description: ビデオ360ビューアのJavaScript APIリファレンス
seo-description: ビデオ360ビューアのJavaScript APIリファレンス
seo-title: setVideo
solution: Experience Manager
title: setVideo
topic: Dynamic media
uuid: 749aa32c-c27f-476c-954b-d4524528bccc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 4%

---


# setVideo{#setvideo}

ビデオ360ビューアのJavaScript APIリファレンス

`setVideo(videoUrl)`

新しい外部ビデオを設定します。 `init()`の前後いつでも呼び出すことができます。 `init()`の後に呼び出すと、ビューアは実行時にビデオを入れ替えます。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)も参照してください。

## パラメータ {#section-b6affc90b3a84584b684641c86862e01}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoUrl  </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>}新しいビデオの絶対URL。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101}を返す

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setVideo("https://s7d9.scene7.com/is/content/Viewers/space_station_360")
```

