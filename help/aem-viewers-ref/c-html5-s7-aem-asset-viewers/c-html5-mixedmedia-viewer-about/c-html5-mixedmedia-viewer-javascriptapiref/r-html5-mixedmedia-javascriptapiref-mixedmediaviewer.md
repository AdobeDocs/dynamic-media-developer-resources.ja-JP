---
description: 混在メディアビューアのJavaScript APIリファレンス。
seo-description: 混在メディアビューアのJavaScript APIリファレンス。
seo-title: MixedMediaViewer
solution: Experience Manager
title: MixedMediaViewer
topic: Dynamic media
uuid: ccaabc04-a9d0-4f58-96bd-ba76e977bfac
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# MixedMediaViewer{#mixedmediaviewer}

混在メディアビューアのJavaScript APIリファレンス。

`MixedMediaViewer([config])`

コンストラクター。新しい混在メディアビューアインスタンスを作成します。

## パラメータ {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 構 </span> 成 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object}オプション </span> のJSON設定オブジェクト。ビューアのすべての設定をコンストラクターに渡し、個々のsetterメソッドを呼び出さないようにします。 次のプロパティが含まれます。 </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <span class="codeph"> containerId </span> - <span class="codeph"> {String}ビュ </span> ーアを挿入するDOMコンテナ(通常は <span class="codeph"> DIV </span>)のID。 このメソッドを呼び出すまでにコンテナ要素を作成しておく必要はありません。 ただし、 <span class="codeph"> init()を実行する際にはコンテナが存在する必 </span> 要があります。 必須。 </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph"> params </span> - <span class="codeph"> {Object} </span> JSONオブジェクト。プロパティ名はビューア固有の設定オプションまたはSDK修飾子で、そのプロパティの値は対応する設定値です。 必須。 </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <span class="codeph"> handlers </span> - <span class="codeph"> {Object} </span> JSONオブジェクトとビューアのイベントコールバック。プロパティ名はサポートされているビューアイベントの名前で、プロパティ値は適切なコールバックへのJavaScript関数参照です。 （オプション） <p>ビューアイベ <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-event-callbacks.md#concept-273d2cddbb7144e284b618ffaf3deabc" format="dita" scope="local"> ントについて詳し </a> くは、イベントコールバックを参照してください。 </p> </li> 
      <li id="li_C592026403804A4FAE12863944A10EE4"> <p> <span class="codeph"> localizedTexts </span> - { <span class="codeph"> Object </span>} JSONオブジェクトとローカリゼーションデータ。 （オプション） </p> <p>詳しくは、ユ <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1" format="dita" scope="local"> ーザーインターフェイス要素のローカ </a> リゼーションを参照してください。 </p> <p>オブジェクトのコ <i>ンテンツについて詳しくは、ビューアSDK</i> User Guideおよび例も参照してください。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
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
"CloseButton.TOOLTIP":"Close" 
}, 
"fr":{ 
"CloseButton.TOOLTIP":"Fermer" 
}, 
defaultLocale:"en" 
} 
});
```

