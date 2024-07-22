---
title: getComponent
description: Video360 ビューア用のJavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: bc5f0046-8e20-4ff0-a90f-05c38f686ad2
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# getComponent{#getcomponent}

Video360 ビューア用のJavaScript API リファレンス。

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
   <td colname="col1"> <p> <span class="codeph"> video360Player </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.Video360Player </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fullScreenButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.FullScreenButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mutableVolume </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.MutableVolume </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> playPauseButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PlayPauseButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoScrubber </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.VideoScrubber </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoTime </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.VideoTime </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> controls </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ControlBar </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> socialShare </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.SocialShare </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> twitterShare </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.TwitterShare </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> facebookShare </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.FacebookShare </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> linkShare </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.LinkShare </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> embedShare </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sk.share.EmbedShare </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

SDK API を使用する場合は、「[ ビューア SDK 名前空間 ](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-viewer-sdk-namespace.md#concept-4ee8657c7d67421f8e7880130a246621)」で説明されているように、正しい完全修飾 SDK 名前空間を使用することが重要です。

特定のコンポーネントについて詳しくは、*HTML5 Viewer SDK API* ドキュメントを参照してください。

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` は、Viewer SDK コンポーネントへのリファレンスです。 `componentId` がサポートされているビューアコンポーネントでない場合や、コンポーネントがまだビューアロジックで作成されていない場合、メソッドは `null` を返します。

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var video360Player = <instance>.getComponent("video360Player"); 
} 
})
```
