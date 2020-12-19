---
description: ビデオ画像ビューアのJavaScript APIリファレンス。
seo-description: ビデオ画像ビューアのJavaScript APIリファレンス。
seo-title: InteractiveImage
solution: Experience Manager
title: InteractiveImage
topic: Dynamic media
uuid: 19bd0603-3180-4913-b5a0-93699c5131bc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 3%

---


# InteractiveImage{#interactiveimage}

ビデオ画像ビューアのJavaScript APIリファレンス。

`InteractiveImage([config])`

コンストラクター。新しいビデオ画像ビューアインスタンスを作成します。

## パラメータ {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} </span> オプションのJSON設定オブジェクトです。個々のセッターメソッドを呼び出さないように、ビューアのすべての設定をコンストラクターに渡すことができます。次のプロパティが含まれます。 </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId  </span> -  <span class="codeph"> {String}ビューアの挿入先のDOMコンテナ(通常は </span> DIV <span class="codeph">  </span>)のID。このメソッドを呼び出すまでに、コンテナ要素を作成する必要はありません。 ただし、<span class="codeph"> init() </span>を実行する場合は、コンテナが存在する必要があります。 </p> <p>必須。 </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> params  </span> -  <span class="codeph"> {Object}ビューアの設定パラメーターを含む </span> JSONオブジェクト。プロパティ名はビューア固有の設定オプションまたはSDK修飾子で、そのプロパティの値は対応する設定値です。 </p> <p>必須。 </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> handlers  </span> -  <span class="codeph"> {Object}ビューアのイベントコールバックを含む </span> JSONオブジェクト。プロパティ名はサポートされているビューアイベントの名前で、プロパティ値は適切なコールバックに対するJavaScript関数参照です。 </p> <p>（オプション） </p> <p>ビューアのイベントについて詳しくは、<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local">イベントコールバック</a>を参照してください。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101}を返す

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
  "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
} 
});
```

