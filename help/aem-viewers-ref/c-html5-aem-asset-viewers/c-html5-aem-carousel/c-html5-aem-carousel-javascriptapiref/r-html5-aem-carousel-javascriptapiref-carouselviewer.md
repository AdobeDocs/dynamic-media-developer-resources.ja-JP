---
description: カルーセルビューアのJavaScript APIリファレンス。
solution: Experience Manager
title: CarouselViewer
feature: Dynamic Media Classic，ビューア，SDK/API，カルーセルバナー
role: Developer,User
exl-id: 890d869d-dbf2-4c24-88d1-34c439ab1e3a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 3%

---

# CarouselViewer{#carouselviewer}

カルーセルビューアのJavaScript APIリファレンス。

`CarouselViewer([config])`

コンストラクター。新しいHTML 5カルーセルビューアインスタンスを作成します。

## パラメータ {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object}オプショ </span> ンのJSON設定オブジェクト。個々のセッターメソッドを呼び出すのを避けるために、すべてのビューア設定をコンストラクターに渡すことができます。次のプロパティが含まれます。 </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId  </span> - { <span class="codeph"> String}ビュ </span> ーアの挿入先のDOMコンテナ(通常は <span class="codeph"> DIV  </span>)のID。このメソッドを呼び出すまでに、コンテナ要素を作成する必要はありません。 ただし、<span class="codeph"> init() </span>を実行する場合は、コンテナが存在する必要があります。 </p> <p>必須。 </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> params  </span> - { <span class="codeph">  </span> Object}ビューアの設定パラメーターを含むJSONオブジェクト。プロパティ名はビューア固有の設定オプションまたはSDK修飾子で、そのプロパティの値は対応する設定値です。 </p> <p>必須。 </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> handlers  </span> -  <span class="codeph">  </span> {Object}ビューアのイベントコールバックを含むJSONオブジェクト。プロパティ名はサポートされているビューアイベントの名前、プロパティ値は適切なコールバックに対するJavaScript関数参照です。 </p> <p>（オプション） </p> <p>ビューアイベントについて詳しくは、 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local">イベントコールバック</a>を参照してください。 </p> </li> 
      <li id="li_CD88EDB586B241DBB87B13709F24C454"> <p> <span class="codeph"> localizedTexts  </span> -  <span class="codeph"> {Object}  </span> </p> <p> ローカリゼーションデータを含むJSONオブジェクト。 オブジェクトのコンテンツについて詳しくは、ユーザーインターフェイス要素のローカライゼーションおよび例を参照してください。 </p> <p>オプション </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
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
