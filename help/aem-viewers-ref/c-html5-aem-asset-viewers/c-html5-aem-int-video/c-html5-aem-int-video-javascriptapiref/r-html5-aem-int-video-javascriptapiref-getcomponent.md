---
description: インタラクティブビデオビューアのJavaScript APIリファレンス。
solution: Experience Manager
title: getComponent
feature: Dynamic Media Classic，ビューア，SDK/API，インタラクティブビデオ
role: Developer,Business Practitioner
exl-id: a760bc86-b700-4ffe-9983-ef55d88677d6
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 1%

---

# getComponent{#getcomponent}

インタラクティブビデオビューアのJavaScript APIリファレンス。

`getComponent(componentId)`

ビューアで使用されるビューアSDKコンポーネントへの参照を返します。 Webページでは、この方法を使用して、標準提供ビューアの動作を拡張またはカスタマイズできます。 このメソッドは、`initComplete`ビューアのコールバックを実行した後にのみ呼び出します。そうしないと、ビューアのロジックによってコンポーネントがまだ作成されていない可能性があります。

## パラメータ {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*`  - `{String}` ビューアで使用されるビューアSDKコンポーネントのID。このビューアは、次のコンポーネントIDをサポートしています。

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>コンポーネントID </p> </th> 
   <th colname="col2" class="entry"> <p>ビューアSDKコンポーネントのクラス名 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameterManager  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> コンテナ </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Container  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mediaSet  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoPlayer  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.VideoPlayer  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> interactiveSwatches  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.InteractiveSwatches  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> callToAction  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.CallToAction  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fullScreenButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.FullScreenButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mutableVolume  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.MutableVolume  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> playPauseButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PlayPauseButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoScrubber  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.VideoScrubber  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoTime  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.VideoTime  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> closedCaptionButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ClosedCaptionButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> コントロール </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ControlBar  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> socialShare  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.SocialShare  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> twitterShare  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.TwitterShare  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> facebookShare  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.FacebookShare  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> linkShare  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.LinkShare  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

SDK APIを操作する場合は、[ビューアSDKの名前空間](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-html5-viewer-sdk-namespace.md#concept-4ee8657c7d67421f8e7880130a246621)で説明されているように、正しい完全修飾SDK名前空間を使用することが重要です。

特定のコンポーネントについて詳しくは、 *ビューアSDK API*&#x200B;のドキュメントを参照してください。

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` ビューアSDKコンポーネントへのリファレンス。`componentId`がサポートされているビューアコンポーネントでない場合、またはビューアのロジックによってコンポーネントがまだ作成されていない場合、メソッドは`null`を返します。

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var videoPlayer = <instance>.getComponent("videoPlayer"); 
} 
})
```
