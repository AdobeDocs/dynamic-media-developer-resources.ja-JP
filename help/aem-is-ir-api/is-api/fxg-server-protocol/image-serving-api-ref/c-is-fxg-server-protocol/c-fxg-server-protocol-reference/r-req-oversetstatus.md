---
description: リクエストのタイプ。 リクエストのタイプを指定します。
seo-description: リクエストのタイプ。 リクエストのタイプを指定します。
seo-title: req
solution: Experience Manager
title: req
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 1c8ff9c3-9f39-46a8-bd38-8e0c5ab0f548
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 2%

---


# req{#req}

リクエストのタイプ。 リクエストのタイプを指定します。

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
   <td colname="col2"> <p> 提供されたURL修飾子を含むfxgのレンダリングに関するエラーを返します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 内容</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7:element</span>属性値と、fxgドキュメント内のすべてのページのリストを持つすべての要素のxmlリストを返します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> &lt;RichText/&gt;</span>要素がオーバーセットされているXMLリストを返します。 </p> <p>クライアント側で処理するためにオーバーセットされた<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>要素のxmlリストを返します。 オーバーセットされた<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>要素のみが返されます。 <span class="+ topic/ph pr-d/codeph codeph"> s7:</span> elementidは、 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> req=oversetstatusを使用する場合に必須の <span class="+ topic/ph pr-d/codeph codeph"> 属性です</span>。<span class="+ topic/ph pr-d/codeph codeph"> s7:elementid </span>を持たないオーバーセット<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>要素は一覧に表示されません。 リスト内の各<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>要素には、<span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>、<span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span>、およびオーバーセットテキストフレームのバウンディングボックスが含まれます。 <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span>属性は、フレームに収まるテキストのストーリー内のテキストインデックスを示します。 <span class="+ topic/ph pr-d/codeph codeph"> Req=</span> oversetstatusonlyは、要求されたFXG内の <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 要素にのみ適用されます。埋め込まれたFXGの<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>要素はリストされません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 存在</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>reqId一意のリクエスト識別子 </p> <p>catalogRecord.existsという名前の1つのプロパティを返します。 指定したカタログエントリが画像または初期設定のカタログに存在する場合、プロパティ値は「1」に設定され、それ以外の場合は「0」に設定されます。 /is/contentコンテキストに対するreq=existsリクエストは、静的コンテンツカタログ内の指定されたレコードの存在または存在を示します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

