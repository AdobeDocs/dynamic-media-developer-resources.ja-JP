---
description: リクエストのタイプ。 リクエストのタイプを指定します。
seo-description: リクエストのタイプ。 リクエストのタイプを指定します。
seo-title: req
solution: Experience Manager
title: req
topic: Scene7 Image Serving - Image Rendering API
uuid: 1c8ff9c3-9f39-46a8-bd38-8e0c5ab0f548
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
   <td colname="col2"> <p> 指定されたURL修飾子を使用したfxgのレンダリングに関するエラーを返します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 内容</span> </p> </td> 
   <td colname="col2"> <p> s7:element属性値を持つすべての要素のxml <span class="codeph"> リストと</span> 、fxgドキュメント内のすべてのページのlistを返します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p>&lt;RichText/&gt;要素がオーバーセ <span class="codeph"> ットされているXMLリスト</span> を返します。 </p> <p>クライアント側で処理するた <span class="+ topic/ph pr-d/codeph codeph"> めにオーバーセットされた</span> &lt;RichText/&gt;要素のxmlリストを返します。 オーバ <span class="+ topic/ph pr-d/codeph codeph"> ーセットの</span> &lt;RichText/&gt;要素のみが返されます。 <span class="+ topic/ph pr-d/codeph codeph"> s7:elementidは、</span> req=oversetstatusを使用する場合に必須の&lt;RichText/&gt; <span class="+ topic/ph pr-d/codeph codeph"> 属性</span> です <span class="+ topic/ph pr-d/codeph codeph"></span>。 <span class="+ topic/ph pr-d/codeph codeph"> s7:elementidを持たない</span> &lt;RichText/&gt;オーバーセット要素は <span class="+ topic/ph pr-d/codeph codeph"></span> 一覧に表示されません。 リス <span class="+ topic/ph pr-d/codeph codeph"> ト内の各</span> &lt;RichText/&gt;要素には、 <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>、 <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span>、およびオーバーセットテキストフレームの境界ボックスが含まれます。 s7:endCharIndex <span class="+ topic/ph pr-d/codeph codeph"></span> 属性は、フレームに収まるまでのテキストのストーリー内のテキストインデックスを示します。 <span class="+ topic/ph pr-d/codeph codeph"> Req=oversetstatusは</span> 、要求され <span class="+ topic/ph pr-d/codeph codeph"> たFXGの&lt;RichText/&gt;</span> 要素にのみ適用されます。 埋め込みFXGの&lt;RichText/&gt; <span class="+ topic/ph pr-d/codeph codeph"> 要素は一覧に表示されません</span> 。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 存在</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>reqId一意のリクエスト識別子 </p> <p>catalogRecord.existsという名前の1つのプロパティを返します。 指定したカタログエントリが画像または初期設定のカタログに存在する場合、プロパティ値は「1」に設定され、それ以外の場合は「0」に設定されます。 /is/contentコンテキストに対するreq=existsリクエストは、静的コンテンツカタログ内の指定されたレコードの存在または存在を示します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

