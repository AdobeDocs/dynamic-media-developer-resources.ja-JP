---
description: フライアウトビューアのJavaScript APIリファレンス。
solution: Experience Manager
title: FlyoutViewer
feature: Dynamic Media Classic，ビューア，SDK/API，フライアウト
role: Developer,Business Practitioner
exl-id: b64f16c8-03bf-4603-972f-845a4c1e2b02
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 3%

---

# FlyoutViewer{#flyoutviewer}

フライアウトビューアのJavaScript APIリファレンス。

`FlyoutViewer([config])`

コンストラクタ；新しいフライアウトビューアインスタンスを作成します。

## パラメータ {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object}オプショ </span> ンのJSON設定オブジェクトです。個々のセッターメソッドを呼び出すのを避けるために、ビューアのすべての設定をコンストラクターに渡すことができます。次のプロパティが含まれます。 </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <span class="codeph"> containerId  </span> - { <span class="codeph"> String}ビュ </span> ーアの挿入先のDOMコンテナ(通常は <span class="codeph"> DIV  </span>)のID。このメソッドを呼び出すまでにコンテナ要素を作成する必要はありません。 ただし、<span class="codeph"> init() </span>を実行する場合は、コンテナが存在する必要があります。 必須。 </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph"> params  </span> - { <span class="codeph">  </span> Object}ビューアの設定パラメーターを含むJSONオブジェクト。プロパティ名はビューア固有の設定オプションまたはSDK修飾子で、そのプロパティの値は対応する設定値です。必須。 </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <span class="codeph"> handlers  </span> -  <span class="codeph">  </span> {Object}ビューアのイベントコールバックを含むJSONオブジェクト。プロパティ名はサポートされているビューアイベントの名前で、プロパティ値は適切なコールバックに対するJavaScript関数参照です。（オプション） <p>ビューアイベントについて詳しくは、 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-event-callbacks.md#concept-53eb01d28189437790268da4929f2a10" format="dita" scope="local">イベントコールバック</a>を参照してください。 </p> </li> 
      <li id="li_218F9597A60249AEBA43A9E86EAFF8BA"> <p> <span class="codeph"> localizedTexts  </span> - {  <span class="codeph"> Object} JSONオブジェクトとローカ </span>ライゼーションデータ。（オプション） </p> <p>詳しくは、 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27" format="dita" scope="local">ユーザーインターフェイス要素のローカライゼーション</a>を参照してください。 </p> <p>オブジェクトのコンテンツについて詳しくは、『<i>ビューアSDKユーザーガイド</i>』と例を参照してください。 （オプション） </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var flyoutViewer = new s7viewers.FlyoutViewer({ 
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
"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom" 
}, 
"fr":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer" 
}, 
defaultLocale:"en" 
} 
});
```
