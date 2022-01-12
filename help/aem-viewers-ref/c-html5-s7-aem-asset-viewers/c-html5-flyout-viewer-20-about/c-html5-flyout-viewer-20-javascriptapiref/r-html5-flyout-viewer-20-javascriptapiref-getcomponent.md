---
title: getComponent
description: フライアウトビューアの JavaScript API リファレンス
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 618d34af-32d0-45bd-928d-7a4e084edbe6
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 1%

---

# getComponent{#getcomponent}

フライアウトビューアの JavaScript API リファレンス

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

SDK API を操作する場合は、「 [Viewer SDK](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-namespace.md#concept-453501a601634dd1bca7b96878c22605).

特定のコンポーネントについて詳しくは、 Viewer SDK API のドキュメントを参照してください。

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
