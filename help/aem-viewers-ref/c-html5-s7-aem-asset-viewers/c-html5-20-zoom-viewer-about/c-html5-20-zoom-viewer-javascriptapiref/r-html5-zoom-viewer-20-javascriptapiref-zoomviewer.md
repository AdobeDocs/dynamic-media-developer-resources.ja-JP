---
title: ZoomViewer
description: ズームビューア用のJavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: fa52a017-0748-4e4f-8d91-ad1529fbfbdb
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 3%

---

# ZoomViewer{#zoomviewer}

ズームビューア用のJavaScript API リファレンス。

`ZoomViewer([config])`

コンストラクタで、ズーム・ビューア・インスタンスを作成します。

## パラメーター {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span> </span> </p> </td> 
   <td colname="col2"> <p> オプション </span>JSON 設定オブジェクトを {object} 用する <span class="codeph">、すべてのビューア設定をコンストラクターに渡して、個々の setter メソッドを呼び出さないようにできます。 次のプロパティが含まれます。 </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <span class="codeph"> containerId </span> - <span class="codeph"> {String} ビューア </span> 挿入する DOM コンテナの ID （通常は <span class="codeph"> DIV </span>）。 このメソッドが呼び出される時点で、コンテナ要素を作成する必要はありません。 ただし、init （） </span> が実行される場合 <span class="codeph"> コンテナが存在する必要があります。 必須。 </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <span class="codeph"> params </span> - <span class="codeph"> {Object} ビューア設定パラメーターを持つ JSON オブジェクトを </span> します。プロパティ名はビューア固有の設定オプションまたは SDK 修飾子で、そのプロパティの値は対応する設定値です。 必須。 </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <span class="codeph"> handlers </span> - <span class="codeph"> {Object} ビューアイベントコールバックを持つ JSON オブジェクトを </span> します。プロパティ名はサポートされているビューアイベントの名前で、プロパティ値は適切なコールバックへのJavaScript関数参照です。 オプション。 <p>ビューアイベントについて詳しくは、<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> Event callbacks </a> を参照してください。 </p> </li> 
      <li id="li_1D181A6B1D434B29B09AFD3F4BE059BD"> <span class="codeph"> localizedTexts </span> - ローカライゼーションデータ </span> 含む JSON オブジェクトを <span class="codeph"> {Object} します。 オプション。 <p>詳 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> くは、ユーザーインターフェイス要素のローカライゼーション </a> を参照してください。 </p> <p><i>Viewer SDK User Guide</i> も参照してください。また、オブジェクトのコンテンツに関する詳細は、例を参照してください。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var zoomViewer = new s7viewers.ZoomViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
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
