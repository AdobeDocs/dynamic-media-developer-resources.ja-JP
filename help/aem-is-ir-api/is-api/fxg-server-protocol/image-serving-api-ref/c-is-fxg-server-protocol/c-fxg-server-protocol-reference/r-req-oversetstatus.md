---
title: 要
description: リクエストタイプ。 リクエストのタイプを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9242c873-5a85-4ede-82b6-4ef15feecf50
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---

# 要{#req}

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
   <td colname="col1"> <p> 検証 <span class="codeph"> る </span> </p> </td> 
   <td colname="col2"> <p> 指定された URL 修飾子で fxg をレンダリングした際にエラーが発生した場合は、それを返します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の内容 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7:element</span> 属性値を持つすべての要素の xml リストと、fxg ドキュメント内のすべてのページのリストを返します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p>&lt;RichText/&gt;<span class="codeph"> 要素がオーバーセットされ </span>XML リストを返します。 </p> <p>クライアント側で処理 <span class="+ topic/ph pr-d/codeph codeph"> るためにオーバーセットされた &lt;RichText/&gt;</span> 要素の xml リストを返します。 オーバーセッ <span class="+ topic/ph pr-d/codeph codeph"> されている &lt;RichText/&gt;</span> 要素のみが返されます。 <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> は、req=oversetstatus<span class="+ topic/ph pr-d/codeph codeph"> を使用する場合 </span> 必須の <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> 属性です。 <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span><span class="+ topic/ph pr-d/codeph codeph"> ない &lt;RichText/&gt;</span> 要素のオーバーセットはリストされません。 リストの各 <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> 要素には、<span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>、<span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span>、およびオーバーセットテキストフレームのバウンディングボックスがあります。 <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> 属性は、ストーリー内のテキストインデックスを示します。テキストは、フレーム内に収まるまでストーリー内のテキストインデックスを示します。 <span class="+ topic/ph pr-d/codeph codeph"> Req=oversetstatus</span> は、リクエストされた FXG の <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> 要素にのみ適用されます。 埋め込まれた FXG の <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> 要素はリストされません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> が存在する </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>reqId の一意のリクエスト識別子 </p> <p>catalogRecord.exists という名前の 1 つのプロパティを返します。 指定したカタログエントリが画像またはデフォルトのカタログに存在する場合、プロパティ値は「1」に設定されます。存在しない場合は、「0」に設定されます。 req=exists、/is/content context に対するリクエストは、静的コンテンツカタログ内の指定されたレコードの有無を示します。 </p> </td> 
  </tr> 
 </tbody> 
</table>
