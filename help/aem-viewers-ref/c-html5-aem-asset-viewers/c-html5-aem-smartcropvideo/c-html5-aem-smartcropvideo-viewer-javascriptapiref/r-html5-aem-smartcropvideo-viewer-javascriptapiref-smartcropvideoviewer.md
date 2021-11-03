---
title: SmartCropVideoViewer
description: スマート切り抜きビデオビューアの JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 4ba152e6-b5a9-4e81-b9f8-aa987a1c31f9
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 3%

---

# SmartCropVideoViewer{#smartcropvideoviewer}

スマート切り抜きビデオビューアの JavaScript API リファレンス。

`SmartCropVideoViewer([config])`

コンストラクタ；スマート切り抜きビデオビューアインスタンスを作成します。

## パラメータ {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> オプションの JSON 設定オブジェクト。すべてのビューア設定をコンストラクターに渡し、個々のセッターメソッドを呼び出さないようにします。 次のプロパティが含まれます。 </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> DOM コンテナの ID ( 通常は <span class="codeph"> DIV </span>) をクリックします。 このメソッドを呼び出すまでにコンテナ要素を作成する必要はありません。 ただし、コンテナは、 <span class="codeph"> init() </span> が実行されます。 必須。 </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph"> params </span> - <span class="codeph"> {Object} </span> ビューアの設定パラメーターを持つ JSON オブジェクト。このプロパティ名はビューア固有の設定オプションまたは SDK 修飾子で、そのプロパティの値は対応する設定値です。 必須。 </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <span class="codeph"> ハンドラー </span> - <span class="codeph"> {Object} </span> ビューアイベントコールバックを含む JSON オブジェクト。プロパティ名はサポートされているビューアイベントの名前で、プロパティ値は適切なコールバックへの JavaScript 関数参照です。 （オプション） <p>詳しくは、 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-event-callbacks.md#concept-ebe5a4c1853d4912a919d86df35c1f6d" format="dita" scope="local"> イベントコールバック </a> を参照してください。 </p> </li> 
      <li id="li_D344288C9B584E569F7BF92D960F9DF8"> <p> <span class="codeph"> localizedTexts </span> - { <span class="codeph"> オブジェクト </span>} ローカリゼーションデータを含む JSON オブジェクト。 （オプション） </p> <p>詳しくは、 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-namespace.md#concept-679bfabb3e3e4c12a285c4e9c4144153" format="dita" scope="local"> Viewer SDK の名前空間 </a> を参照してください。 </p> <p>詳しくは、 <i>ビューア SDK ユーザーガイド</i> と例を参照してください。 （オプション） </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
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
"SmartCropVideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played." 
}, 
"fr":{ 
"SmartCropVideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus." 
}, 
defaultLocale:"en" 
} 
});
```
