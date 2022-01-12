---
title: getComponent
description: インラインズームビューアの JavaScript API リファレンス
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 72ae83e4-b879-4b3b-a5d9-38ed0fc2969d
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 1%

---

# getComponent{#getcomponent}

インラインズームビューアの JavaScript API リファレンス

`getComponent(componentId)`

ビューアで使用される Viewer SDK コンポーネントへの参照を返します。 Web ページでは、この方法を使用して、標準提供ビューアの動作を拡張またはカスタマイズできます。 このメソッドを呼び出すのは、 `initComplete` ビューアコールバックが実行されました。そうしないと、ビューアのロジックによってまだコンポーネントが作成されていない場合があります。

## パラメータ {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*` - `{String}` ビューアで使用されるビューア SDK コンポーネントの ID。 このビューアでは、次のコンポーネント ID がサポートされています。

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>コンポーネント ID </p> </th> 
   <th colname="col2" class="entry"> <p>ビューア SDK のコンポーネントのクラス名 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameterManager </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> コンテナ </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Container </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mediaSet </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> flyout </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.FlyoutZoomView </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> スウォッチ </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.Swatches </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

SDK API を操作する場合は、完全修飾 SDK 名前空間を正しく使用することが重要です。詳しくは、 [Viewer SDK](../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-namespace.md#concept-5af3b472b320496d87735ea612edda80).

特定のコンポーネントについて詳しくは、 Viewer SDK のドキュメントを参照してください。

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Viewer SDK コンポーネントへのリファレンス。 メソッドはを返します。 `null` ( `componentId` はサポートされていないビューアコンポーネントです。または、ビューアのロジックによってコンポーネントがまだ作成されていない場合も同様です。

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var flyoutZoomView = <instance>.getComponent("flyout"); 
} 
})
```
