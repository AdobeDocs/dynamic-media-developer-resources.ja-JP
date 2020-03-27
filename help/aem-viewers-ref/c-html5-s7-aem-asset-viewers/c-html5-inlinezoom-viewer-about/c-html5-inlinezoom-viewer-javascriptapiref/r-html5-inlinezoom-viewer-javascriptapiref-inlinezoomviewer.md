---
description: インラインズームビューアのJavaScript APIリファレンス。
seo-description: インラインズームビューアのJavaScript APIリファレンス。
seo-title: FlyoutViewer
solution: Experience Manager
title: FlyoutViewer
topic: Dynamic media
uuid: 23617eda-f4c9-4908-9f63-593849c12fc7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutViewer{#flyoutviewer}

インラインズームビューアのJavaScript APIリファレンス。

`FlyoutViewer([config])`

コンストラクタ；新しいインラインズームビューアインスタンスを作成します。

## パラメータ {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 構 </span> 成 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object}オプション </span> のJSON設定オブジェクト。ビューアのすべての設定をコンストラクターに渡し、個々のsetterメソッドを呼び出さないようにします。 次のプロパティが含まれます。 </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <span class="codeph"> containerId </span> - <span class="codeph"> {String}ビュ </span> ーアを挿入するDOMコンテナ(通常は <span class="codeph"> DIV </span>)のID。 このメソッドを呼び出すまでにコンテナ要素を作成しておく必要はありません。 ただし、 <span class="codeph"> init()を実行する際にはコンテナが存在する必 </span> 要があります。 必須。 </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph"> params </span> - <span class="codeph"> {Object} </span> JSONオブジェクト。プロパティ名はビューア固有の設定オプションまたはSDK修飾子で、そのプロパティの値は対応する設定値です。 必須。 </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <span class="codeph"> handlers </span> - <span class="codeph"> {Object} </span> JSONオブジェクトとビューアのイベントコールバック。プロパティ名はサポートされているビューアイベントの名前で、プロパティ値は適切なコールバックへのJavaScript関数参照です。 （オプション） <p>ビューアイベ <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-event-callbacks.md#concept-53eb01d28189437790268da4929f2a10" format="dita" scope="local"> ントについて詳し </a> くは、イベントコールバックを参照してください。 </p> </li> 
      <li id="li_218F9597A60249AEBA43A9E86EAFF8BA"> <p> <span class="codeph"> localizedTexts </span> - { <span class="codeph"> Object </span>} JSONオブジェクトとローカリゼーションデータ。 （オプション） </p> <p>詳しくは、ユ <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27" format="dita" scope="local"> ーザーインターフェイス要素のローカ </a> リゼーションを参照してください。 </p> <p>オブジェクトのコ <i>ンテンツについて詳しくは、ビューアSDK</i> SDKユーザガイドおよび例を参照してください。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
"config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
"contenturl" : "http://s7d1.scene7.com/is/content/", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom" 
}, 
"fr":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer" 
}, 
defaultLocale:"en" 
} 
});
```

