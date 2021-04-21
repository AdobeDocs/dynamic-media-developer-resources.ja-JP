---
description: イベントコールバック
solution: Experience Manager
title: イベントコールバック
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,Business Practitioner
exl-id: 59b8a88e-0139-4981-bfb9-f2dc1ac2337d
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 1%

---

# イベントコールバック{#event-callbacks}

ビューアでは、Webページでビューアの初期化プロセスや実行時の動作の追跡に使用されるJavaScriptイベントコールバックがサポートされています。

コールバックハンドラーは、イベント名と`handlers`プロパティを持つ対応するハンドラー関数を、ビューアのコンストラクター内の`config` JSONオブジェクトに渡すことで割り当てられます。 または、`setHandlers()` APIメソッドを使用できます。

サポートされるビューアイベントは次のとおりです。

<table id="table_D4A2035B65B140F882F550B711BD3160"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ビューアイベント </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> initComplete  </span> </p> </td> 
   <td colname="col2"> <p>ビューアの初期化が完了し、すべての内部コンポーネントが作成されたときのトリガー。これにより、<span class="codeph"> getComponent() </span> APIを使用できます。 このコールバックハンドラーは引数を取りません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> trackEvent </span> </p> </td> 
   <td colname="col2"> <p> Adobe Analyticsなどのイベントトラッキングシステムで処理できるイベントがビューア内で発生するたびにトリガーが発生します。 このコールバックハンドラーは次の引数を受け付けます。 </p> <p> 
     <ul id="ul_8A5F409E32E94063AE8D3AB158A0E13D"> 
      <li id="li_1311D5DDD4454FBC9116BA8E2CB003B1"> <p> <span class="codeph"> objID {String}  </span>  — 現在は使用されていません。 </p> </li> 
      <li id="li_C2ABD13097FA40A7B9801C0B7592FB59"> <p> <span class="codeph"> compClass {String}  </span>  — 現在は使用されていません。 </p> </li> 
      <li id="li_3BE8001365714C3FAC32C9B2CFFD5DCE"> <p> <span class="codeph"> instName {String}  </span> -イベントをトリガーしたビューアSDKコンポーネントのインスタンス名。 </p> </li> 
      <li id="li_755DDE84B1CC4B4D8A3FA0C774CBA666"> <p> <span class="codeph"> timeStamp {Number}  </span> -イベントのタイムスタンプ。 </p> </li> 
      <li id="li_05A1C45826AC4D1192CB72FE07EE4C29"> <p> <span class="codeph"> eventInfo {String}  </span> -イベントペイロード。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> quickViewActivate  </span> </p> </td> 
   <td colname="col2"> <p> トリガーは、クイック表示データが関連付けられたホットスポットをアクティブにしたときに表示されます。 このコールバックハンドラーは次の引数を取ります。 </p> <p> 
     <ul id="ul_171110934BD54839B371FAD8D2AD467B"> 
      <li id="li_7B14C3BA432B43E392AC103926807E88"> <p> <span class="codeph"> data {Object}  </span>  — ホットスポット定義のデータを含むJSONオブジェクト。<span class="codeph"> sku </span>フィールドは必須ですが、他のフィールドはオプションで、ソースのホットスポット定義によって異なります。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

[InteractiveImage](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-javascriptapiref/r-html5-aem-int-image-viewer-javascriptapiref-interactiveimage.md#reference-bd16cadc0c054fafb0db4994741d47cd)および[setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-javascriptapiref/r-html5-aem-int-image-viewer-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643)も参照してください。
