---
description: eCatalog SearchViewerのJavaScript API リファレンス。
solution: Experience Manager
title: eCatalogSearchViewer
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: a7289d23-b2f6-4730-99fa-331174968e05
TQID: 'https://experienceleague.adobe.com/mpH1chEHyol7OHeHtR57-rCGYvEM43B2zz2t-ld11zA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 206
ht-degree: 2%

---

# eCatalogSearchViewer{#ecatalogsearchviewer}

eCatalog SearchViewerのJavaScript API リファレンス。

[!DNL `eCatalogSearchViewer([config])`]

コンストラクターは、新しいeCatalog Search Viewer インスタンスを作成します。

## パラメーター {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">設定</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> オプションのJSON設定オブジェクト。すべてのビューア設定をコンストラクターに渡し、個々のセッターメソッドの呼び出しを回避できます。 次のプロパティが含まれます。 </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <p> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ビューアが挿入されているDOM コンテナ （通常は<span class="codeph"> DIV </span>）のID。 このメソッドが呼び出されるまでにコンテナ要素を作成する必要はありません。 ただし、<span class="codeph"> init （） </span>が実行されている場合は、コンテナが存在する必要があります。 必須。 </p> </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <p> <span class="codeph"> パラメーター</span> - <span class="codeph"> {Object} </span> JSON オブジェクトで、プロパティ名がビューア固有の設定オプションまたはSDK修飾子のいずれかであり、そのプロパティの値が対応する設定値であるビューア設定パラメーターを持ちます。 必須。 </p> </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <p> <span class="codeph"> ハンドラー</span> - <span class="codeph"> {Object} </span> ビューア イベント コールバックを持つJSON オブジェクト。プロパティ名はサポートされているビューア イベントの名前で、プロパティ値は適切なコールバックへのJavaScript関数参照です。 オプション。 </p> <p>ビューアイベントの詳細については、<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-event-callbacks.md#concept-0bf5ff877043468db58ac62a92d002b6" format="dita" scope="local"> イベントコールバック </a>を参照してください。 </p> </li> 
      <li id="li_FE5B330E98834CB08C16FCA694F31BE3"> <p> ローカライゼーションデータを含む<span class="codeph"> localizedText </span> - { <span class="codeph"> Object </span> JSON オブジェクト。 オプション。 </p> <p>詳しくは、<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> ユーザーインターフェイス要素</a>のローカライズを参照してください。 </p> <p>オブジェクトの内容について詳しくは、<i>Viewer SDK ユーザーガイド </i>および例も参照してください。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返品 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/", 
 "searchserverurl":"https://s7search1.scene7.com/s7search/" 
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
