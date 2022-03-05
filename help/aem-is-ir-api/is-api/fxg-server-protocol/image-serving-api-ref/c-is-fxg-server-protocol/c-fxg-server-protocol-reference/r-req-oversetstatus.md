---
description: リクエストタイプ。 リクエストのタイプを指定します。
solution: Experience Manager
title: req
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9242c873-5a85-4ede-82b6-4ef15feecf50
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '240'
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
   <td colname="col2"> <p> 指定された URL 修飾子を使用して FXG をレンダリングする際にエラーが発生した場合に返されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 内容</span> </p> </td> 
   <td colname="col2"> <p> すべての要素の xml リストを <span class="codeph"> s7:element</span> 属性値と fxg ドキュメント内のすべてのページのリスト。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p>次の XML リストを返します。 <span class="codeph"> &lt;richtext /&gt;</span> 要素がオーバーセットされます。 </p> <p>次の XML リストを返します： <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> クライアント側で処理するためにオーバーセットされる要素。 のみ <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> オーバーセットされた要素が返されます。 <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> は必須です <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 使用時の属性 <span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span>. オーバーセット <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 要素 <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> が一覧に表示されていません。 各 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> リスト内の要素に <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>, <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span>、およびオーバーセットテキストフレームの境界ボックス。 この <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> 属性は、ストーリー内のテキストがフレームに収まるまでのテキストインデックスを示します。 <span class="+ topic/ph pr-d/codeph codeph"> Req=oversetstatus</span> のみに適用 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 要求された FXG 内の要素。 リストには、 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 埋め込み FXG からの要素。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 存在</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>reqId 一意のリクエスト識別子 </p> <p>catalogRecord.exists という名前の単一のプロパティを返します。 指定したカタログエントリが画像またはデフォルトのカタログに存在する場合、プロパティ値は「1」に設定され、存在しない場合は「0」に設定されます。 /is/content コンテキストに対する req=exists リクエストは、静的コンテンツカタログ内の指定されたレコードの有無を示します。 </p> </td> 
  </tr> 
 </tbody> 
</table>
