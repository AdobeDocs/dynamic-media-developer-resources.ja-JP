---
title: CarouselViewer
description: カルーセルビューアのJavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 890d869d-dbf2-4c24-88d1-34c439ab1e3a
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 3%

---

# CarouselViewer{#carouselviewer}

カルーセルビューアのJavaScript API リファレンス。

`CarouselViewer([config])`

コンストラクターを使用して、HTML 5 カルーセルビューアインスタンスを作成します。

## パラメーター {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span> </span> </p> </td> 
   <td colname="col2"> <p> オプション </span>JSON 設定オブジェクトを {object} 用する <span class="codeph">、すべてのビューア設定をコンストラクターに渡して、個々の setter メソッドを呼び出さないようにできます。 次のプロパティが含まれます。 </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId </span> - <span class="codeph"> {String} ビューア </span> 挿入する DOM コンテナの ID （通常は <span class="codeph"> DIV </span>）。 このメソッドが呼び出される時点で、コンテナ要素を作成する必要はありません。 ただし、init （） </span> が実行される場合 <span class="codeph"> コンテナが存在する必要があります。 </p> <p>必須。 </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> params </span> - <span class="codeph"> {Object} ビューア設定パラメーターを持つ JSON オブジェクトを </span> します。プロパティ名はビューア固有の設定オプションまたは SDK 修飾子で、そのプロパティの値は対応する設定値です。 </p> <p>必須。 </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> handlers </span> - <span class="codeph"> {Object} ビューアイベントコールバックを持つ JSON オブジェクトを </span> します。プロパティ名はサポートされているビューアイベントの名前で、プロパティ値は適切なコールバックへのJavaScript関数参照です。 </p> <p>オプション。 </p> <p>ビューアイベントについて詳しくは、<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> Event callbacks </a> を参照してください。 </p> </li> 
      <li id="li_CD88EDB586B241DBB87B13709F24C454"> <p> <span class="codeph"> localizedTexts </span> - <span class="codeph"> {Object} </span> </p> <p> ローカリゼーションデータを含む JSON オブジェクト。 オブジェクトのコンテンツについて詳しくは、ユーザーインターフェイス要素のローカライゼーションおよび例を参照してください。 </p> <p>オプション </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"PanLeftButton.TOOLTIP":"Left" 
}, 
"fr":{ 
"PanLeftButton.TOOLTIP":"Gauchiste" 
}, 
defaultLocale:"en" 
} 
});
```
