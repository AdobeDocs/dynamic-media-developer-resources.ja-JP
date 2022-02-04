---
title: SpinViewer
description: スピンビューアの JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 0cfde665-c578-41a0-a428-0db3cbdac6ae
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 3%

---

# SpinViewer{#spinviewer}

スピンビューアの JavaScript API リファレンス。

`SpinViewer([config])`

コンストラクター。新しいスピンビューアインスタンスを作成します。

## パラメータ {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> オプションの JSON 設定オブジェクト。すべてのビューア設定をコンストラクターに渡し、個々のセッターメソッドを呼び出さないようにします。 次のプロパティが含まれます。 </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <p> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> DOM コンテナの ID ( 通常は <span class="codeph"> DIV </span>) をクリックします。 このメソッドを呼び出すまでにコンテナ要素を作成する必要はありません。 ただし、コンテナは、 <span class="codeph"> init() </span> が実行されます。 必須。 </p> </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <p> <span class="codeph"> params </span> - <span class="codeph"> {Object} </span> ビューアの設定パラメーターを持つ JSON オブジェクト。このプロパティ名はビューア固有の設定オプションまたは SDK 修飾子で、そのプロパティの値は対応する設定値です。 必須。 </p> </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <p> <span class="codeph"> ハンドラー </span> - <span class="codeph"> {Object} </span> ビューアイベントコールバックを含む JSON オブジェクト。プロパティ名はサポートされているビューアイベントの名前で、プロパティ値は適切なコールバックへの JavaScript 関数参照です。 （オプション） </p> <p>詳しくは、 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-event-callbacks.md#concept-9c553c80eefd422faacf6522c69804bf" format="dita" scope="local"> イベントコールバック </a> を参照してください。 </p> </li> 
      <li id="li_643787FB4A424D0AB6B8E12F44C3A9AC"> <p> <span class="codeph"> localizedTexts </span> - <span class="codeph"> {Object} </span> ローカリゼーションデータを含む JSON オブジェクト。 （オプション） </p> <p>詳しくは、 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-localization.md#concept-e35c15c9e82648328806cdc6aa255d98" format="dita" scope="local"> ユーザーインターフェイス要素のローカライゼーション </a> を参照してください。 </p> <p>関連トピック <i>ビューア SDK ユーザーガイド</i> と例を参照してください。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

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
