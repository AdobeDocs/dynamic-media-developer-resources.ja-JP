---
title: イベントコールバック
description: イベントコールバック
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: e87b2a84-735c-4412-a4dd-97b18474a1d2
TQID: 'https://experienceleague.adobe.com/VTILhyWja7ccpZeTREmdVA02kApt5VsJPNA-WevQWcM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 212
ht-degree: 1%

---

# イベントコールバック{#event-callbacks}

ビューアは、Web ページがビューアの初期化プロセスまたはランタイム動作をトラッキングするために使用するJavaScript イベントコールバックをサポートしています。

コールバックハンドラーは、`handlers` プロパティを持つイベント名と対応するハンドラー関数をビューアのコンストラクターの`config` JSON オブジェクトに渡すことによって割り当てられます。 または、`setHandlers()` API メソッドを使用することもできます。

サポートされるビューアイベントには、次のものがあります。

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
   <td colname="col2"> <p>ビューアの初期化が完了し、すべての内部コンポーネントが作成されたときにトリガーが発生します。これにより、<span class="codeph"> getComponent （） </span> APIを使用できます。 コールバックハンドラーは引数を受け取りません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> trackEvent </span> </p> </td> 
   <td colname="col2"> <p> Adobe Analyticsなどのイベントトラッキングシステムで処理できるビューア内でイベントが発生するたびにトリガーします。 コールバックハンドラーは次の引数を受け入れます。 </p> <p> 
     <ul id="ul_8A5F409E32E94063AE8D3AB158A0E13D"> 
      <li id="li_1311D5DDD4454FBC9116BA8E2CB003B1"> <p> <span class="codeph"> objID {String} </span> – 現在使用されていません。 </p> </li> 
      <li id="li_C2ABD13097FA40A7B9801C0B7592FB59"> <p> <span class="codeph"> compClass {String} </span> – 現在使用されていません。 </p> </li> 
      <li id="li_3BE8001365714C3FAC32C9B2CFFD5DCE"> <p> <span class="codeph"> instName {String} </span> - イベントをトリガーしたViewer SDK コンポーネントのインスタンス名。 </p> </li> 
      <li id="li_755DDE84B1CC4B4D8A3FA0C774CBA666"> <p> <span class="codeph"> timeStamp {Number} </span> - イベントタイムスタンプ。 </p> </li> 
      <li id="li_05A1C45826AC4D1192CB72FE07EE4C29"> <p> <span class="codeph"> eventInfo {String} </span> - イベントペイロード。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> quickViewActivate </span> </p> </td> 
   <td colname="col2"> <p> クイックビューデータが関連付けられたホットスポットをアクティベートする際のトリガー。 コールバックハンドラーは次の引数を取ります。 </p> <p> 
     <ul id="ul_171110934BD54839B371FAD8D2AD467B"> 
      <li id="li_7B14C3BA432B43E392AC103926807E88"> <p> <span class="codeph"> データ {Object} </span> - ホットスポット定義のデータを含むJSON オブジェクト。 フィールド <span class="codeph"> sku </span>は必須ですが、他のフィールドはオプションで、ソース ホットスポット定義に依存します。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

[CarouselViewer**](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-carouselviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd)および[setHandlers**](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643)も参照してください。
