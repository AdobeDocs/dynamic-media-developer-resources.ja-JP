---
title: getComponent
description: スピンビューアのJavaScript API リファレンス
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: f0cb5a99-814f-4c4d-bfe3-bb670c8f9926
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---

# getComponent{#getcomponent}

スピンビューアのJavaScript API リファレンス

`getComponent(componentId)`

ビューアが使用する Viewer SDK コンポーネントへの参照を返します。 Web ページでは、この方法を使用して、標準ビューアの動作を拡張またはカスタマイズできます。 このメソッドは `initComplete` ビューアコールバックが実行された後にのみ呼び出します。それ以外の場合、コンポーネントはビューアロジックによってまだ作成されていない可能性があります。

## パラメーター {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*` - ビューアが使用する Viewer SDK コンポーネントの ID を `{String}` します。 このビューアは、次のコンポーネント ID をサポートしています。

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>コンポーネント ID </p> </th> 
   <th colname="col2" class="entry"> <p>ビューア SDK コンポーネントのクラス名 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameterManager </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> container </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Container </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mediaSet </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spinView </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.SpinView </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomInButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomInButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomOutButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomOutButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomResetButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomResetButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fullScreenButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.FullScreenButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> closeButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.CloseButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spinLeftButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanLeftButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spinRightButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanRightButton </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

SDK API を使用する場合は、[Viewer SDK](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-namespace.md#concept-fa293878c9ff4758ae888415c70fbeef) に記載されているように、正しい完全修飾 SDK 名前空間を使用することが重要です。

特定のコンポーネントについて詳しくは、Viewer SDK API ドキュメントを参照してください。

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Viewer SDK コンポーネントへのリファレンスです。 `componentId` がサポートされているビューアコンポーネントでない場合や、コンポーネントがまだビューアロジックで作成されていない場合、メソッドは `null` を返します。

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var spinView = <instance>.getComponent("spinView"); 
} 
})
```
