---
title: VideoViewer
description: ビデオビューア用JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 4ba152e6-b5a9-4e81-b9f8-aa987a1c31f9
TQID: 'https://experienceleague.adobe.com/OmRxGHKzfzWln4YYGCwCgVNgezzK4yKJRY1i67sgq8Y'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 203
ht-degree: 3%

---

# VideoViewer{#videoviewer}

ビデオビューア用JavaScript API リファレンス。

`VideoViewer([config])`

コンストラクター。新しいビデオビューアーインスタンスを作成します。

## パラメーター {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">設定</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> オプションのJSON設定オブジェクト。すべてのビューア設定をコンストラクターに渡し、個々のセッターメソッドの呼び出しを回避できます。 次のプロパティが含まれます。 </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ビューアが挿入されているDOM コンテナ （通常は<span class="codeph"> DIV </span>）のID。 このメソッドが呼び出されるまでにコンテナ要素を作成する必要はありません。 ただし、<span class="codeph"> init （） </span>が実行されている場合は、コンテナが存在する必要があります。 必須。 </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph"> パラメーター</span> - <span class="codeph"> {Object} </span> JSON オブジェクトで、プロパティ名がビューア固有の設定オプションまたはSDK修飾子のいずれかであり、そのプロパティの値が対応する設定値であるビューア設定パラメーターを持ちます。 必須。 </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <span class="codeph"> ハンドラー</span> - <span class="codeph"> {Object} </span> ビューア イベント コールバックを持つJSON オブジェクト。プロパティ名はサポートされているビューア イベントの名前で、プロパティ値は適切なコールバックへのJavaScript関数参照です。 オプション。 <p>ビューアイベントの詳細については、<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-event-callbacks.md#concept-ebe5a4c1853d4912a919d86df35c1f6d" format="dita" scope="local"> イベントコールバック </a>を参照してください。 </p> </li> 
      <li id="li_D344288C9B584E569F7BF92D960F9DF8"> <p> ローカライゼーションデータを含む<span class="codeph"> localizedText </span> - &lbrace; <span class="codeph"> Object </span> JSON オブジェクト。 オプション。 </p> <p>詳しくは、<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-namespace.md#concept-679bfabb3e3e4c12a285c4e9c4144153" format="dita" scope="local"> Viewer SDK名前空間</a>を参照してください。 </p> <p>オブジェクトの内容について詳しくは、<i>Viewer SDK ユーザーガイド </i>および例を参照してください。 オプション。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返品 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"VideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played." 
}, 
"fr":{ 
"VideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus." 
}, 
defaultLocale:"en" 
} 
});
```
