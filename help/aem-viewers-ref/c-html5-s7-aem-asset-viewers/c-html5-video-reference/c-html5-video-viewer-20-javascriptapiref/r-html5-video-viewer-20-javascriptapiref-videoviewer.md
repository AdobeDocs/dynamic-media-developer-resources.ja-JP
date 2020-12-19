---
description: ビデオビューアのJavaScript APIリファレンス。
seo-description: ビデオビューアのJavaScript APIリファレンス。
seo-title: VideoViewer
solution: Experience Manager
title: VideoViewer
topic: Dynamic media
uuid: ad180d92-3e5c-4ded-b82b-79c23aa5c597
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 3%

---


# VideoViewer{#videoviewer}

ビデオビューアのJavaScript APIリファレンス。

`VideoViewer([config])`

コンストラクタ；新しいビデオビューアインスタンスを作成します。

## パラメータ {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> オプションのJSON設定オブジェクトです。個々のセッターメソッドを呼び出す必要がないように、ビューアのすべての設定をコンストラクターに渡すことができます。次のプロパティが含まれます。 </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <span class="codeph"> containerId  </span> -  <span class="codeph"> {String}ビューアの挿入先のDOMコンテナ(通常は </span> DIV <span class="codeph">  </span>)のID。このメソッドを呼び出すまでにコンテナ要素を作成しておく必要はありません。 ただし、<span class="codeph"> init() </span>を実行する場合は、コンテナが存在する必要があります。 必須。 </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph"> params  </span> -  <span class="codeph"> {Object}ビューアの設定パラメーターを含む </span> JSONオブジェクト。プロパティ名はビューア固有の設定オプションまたはSDK修飾子で、そのプロパティの値は対応する設定値です。必須。 </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <span class="codeph"> handlers  </span> -  <span class="codeph"> {Object}ビューアのイベントコールバックを含む </span> JSONオブジェクト。プロパティ名はサポートされているビューアイベントの名前で、プロパティ値は適切なコールバックに対するJavaScript関数参照です。（オプション） <p>ビューアのイベントについて詳しくは、<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-event-callbacks.md#concept-ebe5a4c1853d4912a919d86df35c1f6d" format="dita" scope="local">イベントコールバック</a>を参照してください。 </p> </li> 
      <li id="li_D344288C9B584E569F7BF92D960F9DF8"> <p> <span class="codeph"> localizedTexts  </span> - {  <span class="codeph"> Object  </span>} JSONオブジェクトとローカライゼーションデータ。（オプション） </p> <p>詳しくは、<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-namespace.md#concept-679bfabb3e3e4c12a285c4e9c4144153" format="dita" scope="local">ビューアSDK名前空間</a>を参照してください。 </p> <p>オブジェクトのコンテンツについて詳しくは、<i>ビューアSDKユーザガイド</i>および例を参照してください。 （オプション） </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101}を返す

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
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

