---
title: setVideo
description: Video360 ビューア用のJavaScript API リファレンス
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: e1894d96-6f37-4e34-a709-5b0121bd0696
source-git-commit: ce1ac4938c7baf482c6c55a9ad13379153a3ec5b
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 3%

---

# setVideo{#setvideo}

Video360 ビューア用のJavaScript API リファレンス

`setVideo(videoUrl)`

新規外部ビデオを設定します。 `init()` の前と後の両方でいつでも呼び出すことができます。 `init()` 後に呼び出された場合、ビューアは実行時にビデオをスワップします。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6) も参照してください。

## パラメーター {#section-b6affc90b3a84584b684641c86862e01}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoUrl </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} 新しいビデオへの絶対 URL。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし


## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setVideo("https://s7d9.scene7.com/is/content/Viewers/space_station_360")
```

