---
title: BasicZoomViewer
description: 基本ズームビューアの JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 320f740e-c6b9-44d6-9369-9c2ec31189c5
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 3%

---

# BasicZoomViewer{#basiczoomviewer}

基本ズームビューアの JavaScript API リファレンス。

`BasicZoomViewer([config])`

コンストラクタ。基本ズームビューアインスタンスを作成します。

## パラメータ {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} </span> オプションの JSON 設定オブジェクト。個々のセッターメソッドを呼び出すのを避けるために、すべてのビューア設定をコンストラクターに渡すことができます。 次のプロパティが含まれます。 </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> DOM コンテナの ID ( 通常は <span class="codeph"> DIV </span>) をクリックします。 このメソッドを呼び出すまでに、コンテナ要素を作成する必要はありません。 ただし、コンテナは、 <span class="codeph"> init() </span> が実行されます。 必須。 </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> params </span> - <span class="codeph"> {Object} </span> ビューアの設定パラメーターを持つ JSON オブジェクト。プロパティ名はビューア固有の設定オプションまたは SDK 修飾子で、そのプロパティの値は対応する設定値です。 必須。 </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> ハンドラー </span> - <span class="codeph"> {Object} </span> ビューアのイベントコールバックを含む JSON オブジェクト。プロパティ名はサポートされているビューアイベントの名前、プロパティ値は適切なコールバックへの JavaScript 関数参照です。 （オプション） </p> <p>詳しくは、 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-event-callbacks.md#concept-8ba57cf86537401999514e1b221ec734" format="dita" scope="local"> イベントコールバック </a> を参照してください。 </p> </li> 
      <li id="li_528FE03845F847E08F964E38D6AB6E86"> <p> <span class="codeph"> localizedTexts </span> - <span class="codeph"> {Object} </span> ローカリゼーションデータを含む JSON オブジェクト。 （オプション） </p> <p>詳しくは、 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> ユーザーインターフェイス要素のローカライゼーション </a> を参照してください。 </p> <p> 関連トピック <i>ビューア SDK ユーザーガイド</i> と例を参照してください。 オプション </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"Scene7SharedAssets/Backpack_B", 
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
