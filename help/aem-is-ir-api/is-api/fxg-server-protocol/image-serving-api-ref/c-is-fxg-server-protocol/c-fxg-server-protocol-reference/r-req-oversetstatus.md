---
title: req
description: リクエストタイプ： リクエストのタイプを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9242c873-5a85-4ede-82b6-4ef15feecf50
TQID: 'https://experienceleague.adobe.com/uj4dkcoE66sj68VxVb92ncvX9FTQAy99TMUOW-rLc-A'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 245
ht-degree: 0%

---

# req{#req}

リクエストタイプ： リクエストのタイプを指定します。

`req={validate|contents|oversetstatus|exists}`

<table id="table_F39239E5244746DB9F253BB0D5E85D54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 値 </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">検証</span> </p> </td> 
   <td colname="col2"> <p> 指定されたurl修飾子を使用してfxgをレンダリングする際のエラーを返します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">件のコンテンツ </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7:element</span>属性値とfxg ドキュメント内のすべてのページのリストを持つすべての要素のxml リストを返します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> &lt;RichText/&gt;</span>要素がオーバーセットされているXML リストを返します。 </p> <p>クライアント側で処理するためにオーバーセットされている<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>要素のxml リストを返します。 オーバーセットされた<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>要素のみが返されます。 <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>は、<span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span>を使用する場合、<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>属性として必須です。 <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>を持たない<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>要素はリストに含まれません。 リスト内の各<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>要素には、<span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>、<span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span>およびオーバーセットテキストフレームのバウンディングボックスがあります。 <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span>属性は、ストーリー内のテキストインデックスが、どのテキストがフレームに収まることができたかを示します。 <span class="+ topic/ph pr-d/codeph codeph"> Req=oversetstatus</span>は、要求されたFXG内の<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>要素にのみ適用されます。 埋め込まれたFXGの<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>要素はリストされません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">が存在します</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>reqId一意のリクエスト ID </p> <p>catalogRecord.existsという名前の単一のプロパティを返します。 指定したカタログエントリが画像またはデフォルトカタログに存在する場合、プロパティ値は「1」に設定されます。それ以外の場合は「0」に設定されます。 /is/content コンテキストに対するreq=exists リクエストは、静的コンテンツカタログ内の指定されたレコードの有無を示します。 </p> </td> 
  </tr> 
 </tbody> 
</table>
