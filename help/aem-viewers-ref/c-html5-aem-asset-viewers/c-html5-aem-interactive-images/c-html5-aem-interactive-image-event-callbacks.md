---
title: イベントコールバック
description: イベントコールバック
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 59b8a88e-0139-4981-bfb9-f2dc1ac2337d
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 1%

---

# イベントコールバック{#event-callbacks}

ビューアは、JavaScript イベントコールバックをサポートしています。このコールバックは、web ページで、ビューアの初期化プロセスやランタイムの動作のトラッキングに使用されます。

コールバックハンドラーは、`handlers` プロパティを持つイベント名と対応するハンドラー関数をビューアのコンストラクター内 `config`JSON オブジェクトに渡すことによって割り当てられます。 または、API メソッドを使用するこ `setHandlers()` もできます。

次のビューアイベントがサポートされています。

<table id="table_D4A2035B65B140F882F550B711BD3160"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ビューアイベント </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> initComplete </span> </p> </td> 
   <td colname="col2"> <p>トリガー ビューアの初期化が完了し、すべての内部コンポーネントが作成されると、getComponent （） </span> API<span class="codeph"> 使用できるようになります。 コールバックハンドラーは引数を取りません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> trackEvent </span> </p> </td> 
   <td colname="col2"> <p> Adobe Analyticsなどのイベントトラッキングシステムで処理される可能性のあるビューア内でイベントが発生するたびに発生するトリガー。 コールバックハンドラーは、次の引数を受け付けます。 </p> <p> 
     <ul id="ul_8A5F409E32E94063AE8D3AB158A0E13D"> 
      <li id="li_1311D5DDD4454FBC9116BA8E2CB003B1"> <p> <span class="codeph"> objID {String} </span> – 現在使用されていません。 </p> </li> 
      <li id="li_C2ABD13097FA40A7B9801C0B7592FB59"> <p> <span class="codeph"> compClass {String} </span> – 現在使用されていません。 </p> </li> 
      <li id="li_3BE8001365714C3FAC32C9B2CFFD5DCE"> <p> <span class="codeph"> instName {String} </span> - イベントをトリガーしたビューア SDK コンポーネントのインスタンス名。 </p> </li> 
      <li id="li_755DDE84B1CC4B4D8A3FA0C774CBA666"> <p> <span class="codeph"> timeStamp {Number} </span> - イベントタイムスタンプ。 </p> </li> 
      <li id="li_05A1C45826AC4D1192CB72FE07EE4C29"> <p> <span class="codeph"> eventInfo {String} </span> - イベントペイロード。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> quickViewActivate </span> ードの <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> クイックビューデータが関連付けられたホットスポットがアクティブ化されたときのトリガーです。 コールバックハンドラーは次の引数を取ります。 </p> <p> 
     <ul id="ul_171110934BD54839B371FAD8D2AD467B"> 
      <li id="li_7B14C3BA432B43E392AC103926807E88"> <p> <span class="codeph"> data {Object} </span> - ホットスポット定義からのデータを含む JSON オブジェクト。 SKU </span><span class="codeph"> フィールドは必須ですが、その他のフィールドはオプションで、ソースホットスポットの定義によって異なります。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

[InteractiveImage](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-javascriptapiref/r-html5-aem-int-image-viewer-javascriptapiref-interactiveimage.md#reference-bd16cadc0c054fafb0db4994741d47cd) および [setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-javascriptapiref/r-html5-aem-int-image-viewer-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643) も参照してください。
