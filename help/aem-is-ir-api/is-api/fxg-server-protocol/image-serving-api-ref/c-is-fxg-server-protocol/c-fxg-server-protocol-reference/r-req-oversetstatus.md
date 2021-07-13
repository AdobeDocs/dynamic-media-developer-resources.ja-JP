---
description: リクエストタイプ。 リクエストのタイプを指定します。
solution: Experience Manager
title: req
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 9242c873-5a85-4ede-82b6-4ef15feecf50
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 2%

---

# req{#req}

リクエストタイプ。 リクエストのタイプを指定します。

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
   <td colname="col1"> <p> <span class="codeph"> 検証</span> </p> </td> 
   <td colname="col2"> <p> 指定されたURL修飾子を使用してfxgをレンダリングすると、エラーが返されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 内容</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7:element</span>属性値とfxgドキュメント内のすべてのページのリストを持つすべての要素のxmlリストを返します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> &lt;RichText/&gt;</span>要素がオーバーセットされたXMLリストを返します。 </p> <p>クライアント側で処理するためにオーバーセットされた<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>要素のxmlリストを返します。 オーバーセットされた<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>要素のみが返されます。 <span class="+ topic/ph pr-d/codeph codeph"> s7:</span> elementidは、 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> req=oversetstatus <span class="+ topic/ph pr-d/codeph codeph"> を使用する</span>場合に必須の属性です。<span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>を持たないオーバーセット<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>要素はリストに表示されません。 リスト内の各<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>要素には、 <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>、 <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span>およびオーバーセットテキストフレームのバウンディングボックスが含まれます。 <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span>属性は、ストーリー内でテキストがフレームに収まるまでのテキストインデックスを示します。 <span class="+ topic/ph pr-d/codeph codeph"> Req=oversetstatusonly</span> は、要求されたFXG <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 内の要素に適用されます。埋め込みFXGの<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>要素は一覧表示されません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 存在</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>reqId一意のリクエスト識別子 </p> <p>catalogRecord.existsという名前の単一のプロパティを返します。 指定したカタログエントリが画像またはデフォルトのカタログに存在する場合、プロパティ値は「1」に設定され、それ以外の場合は「0」に設定されます。 /is/contentコンテキストに対するreq=existsリクエストは、静的コンテンツカタログ内の指定されたレコードの有無を示します。 </p> </td> 
  </tr> 
 </tbody> 
</table>
