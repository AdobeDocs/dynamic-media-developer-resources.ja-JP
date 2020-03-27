---
description: スピンビューアのJavaScript APIリファレンス。
seo-description: スピンビューアのJavaScript APIリファレンス。
seo-title: SpinViewer
solution: Experience Manager
title: SpinViewer
topic: Dynamic media
uuid: e9048f17-7a2a-4eae-a5a0-df14f16aebc5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinViewer{#spinviewer}

スピンビューアのJavaScript APIリファレンス。

`SpinViewer([config])`

コンストラクター。新しいスピンビューアインスタンスを作成します。

## パラメータ {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 構 </span> 成 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object}オプション </span> のJSON設定オブジェクト。ビューアのすべての設定をコンストラクターに渡し、個々のsetterメソッドを呼び出さないようにします。 次のプロパティが含まれます。 </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <p> <span class="codeph"> containerId </span> - <span class="codeph"> {String}ビュ </span> ーアを挿入するDOMコンテナ(通常は <span class="codeph"> DIV </span>)のID。 このメソッドを呼び出すまでにコンテナ要素を作成しておく必要はありません。 ただし、 <span class="codeph"> init()を実行する際にはコンテナが存在する必 </span> 要があります。 必須。 </p> </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <p> <span class="codeph"> params </span> - <span class="codeph"> {Object} </span> JSONオブジェクト。プロパティ名はビューア固有の設定オプションまたはSDK修飾子で、そのプロパティの値は対応する設定値です。 必須。 </p> </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <p> <span class="codeph"> handlers </span> - <span class="codeph"> {Object} </span> JSONオブジェクトとビューアのイベントコールバック。プロパティ名はサポートされているビューアイベントの名前で、プロパティ値は適切なコールバックへのJavaScript関数参照です。 （オプション） </p> <p>ビューアイベ <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-event-callbacks.md#concept-9c553c80eefd422faacf6522c69804bf" format="dita" scope="local"> ントについて詳し </a> くは、イベントコールバックを参照してください。 </p> </li> 
      <li id="li_643787FB4A424D0AB6B8E12F44C3A9AC"> <p> <span class="codeph"> localizedTexts </span> - <span class="codeph"> {Object} </span> JSONオブジェクトとローカリゼーションデータ。 （オプション） </p> <p>詳しくは、ユ <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-localization.md#concept-e35c15c9e82648328806cdc6aa255d98" format="dita" scope="local"> ーザーインターフェイス要素のローカ </a> リゼーションを参照してください。 </p> <p>オブジェクトのコ <i>ンテンツについて詳しくは、ビューアSDK</i> User Guideおよび例も参照してください。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
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

