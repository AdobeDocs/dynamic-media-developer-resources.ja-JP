---
title: InteractiveVideoViewer
description: インタラクティブビデオビューアのJavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: efd0ffea-482c-4af4-ac77-ac1b7f326ce9
TQID: 'https://experienceleague.adobe.com/sC9HwtnllWM-LX5BSLsBRh8OOjriVKnfEfhtZ8LacdA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 204
ht-degree: 2%

---

# InteractiveVideoViewer{#interactivevideoviewer}

インタラクティブビデオビューアのJavaScript API リファレンス。

`InteractiveVideoViewer([config])`

コンストラクターを使用して、インタラクティブビデオビューアインスタンスを作成します。

## パラメーター {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">設定</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} </span> オプションのJSON設定オブジェクト。すべてのビューア設定をコンストラクターに渡して、個々のセッターメソッドの呼び出しを回避できます。 次のプロパティが含まれます。 </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ビューアが挿入されるDOM コンテナ （通常は<span class="codeph"> DIV </span>）のID。 このメソッドが呼び出される時点では、コンテナ要素を作成する必要はありません。 ただし、<span class="codeph"> init （） </span>が実行されている場合は、コンテナが存在する必要があります。 </p> <p>必須。 </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> パラメーター</span> - <span class="codeph"> {Object} </span> JSON オブジェクトと、ビューア設定パラメーターを持つオブジェクト。プロパティ名はビューア固有の設定オプションまたはSDK修飾子のいずれかであり、そのプロパティの値は対応する設定値です。 </p> <p>必須。 </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> ハンドラー</span> - <span class="codeph"> {Object} </span> ビューア イベント コールバックを持つJSON オブジェクト。プロパティ名はサポートされているビューア イベントの名前で、プロパティ値は適切なコールバックへのJavaScript関数参照です。 </p> <p>オプション。 </p> <p>ビューアイベントの詳細については、<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> イベントコールバック </a>を参照してください。 </p> </li> 
      <li id="li_42A3F3BEF1004E069F0FB2AE0A30B093"> <p> ローカライゼーションデータを含む<span class="codeph"> localizedText </span> - <span class="codeph"> {Object} </span> JSON オブジェクト オプション。 </p> <p>詳しくは、<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> ユーザーインターフェイス要素</a>のローカライズを参照してください。 </p> <p>オブジェクトの内容について詳しくは、<i>Viewer SDK ユーザーガイド </i>および例も参照してください。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返品 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
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
