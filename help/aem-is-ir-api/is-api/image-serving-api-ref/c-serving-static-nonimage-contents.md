---
description: 画像サービングを使用して、カタログ内の画像以外のコンテンツを管理し、個別の/is/contentコンテキストを介して提供できます。
seo-description: 画像サービングを使用して、カタログ内の画像以外のコンテンツを管理し、個別の/is/contentコンテキストを介して提供できます。
seo-title: 静的な（画像以外の）コンテンツの提供
solution: Experience Manager
title: 静的な（画像以外の）コンテンツの提供
topic: Scene7 Image Serving - Image Rendering API
uuid: bdb1383a-e02d-499f-be79-4a6dc501705c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---


# 静的な（画像以外の）コンテンツの提供{#serving-static-non-image-contents}

画像サービングを使用して、カタログ内の画像以外のコンテンツを管理し、個別の/is/contentコンテキストを介して提供できます。

この機能を使用すると、各項目のTTLを個別に設定できます。

画像サービングは、[!DNL /is/content]で次のコマンドをサポートしています。

<table id="simpletable_8A3AB1D1D20F4B6CBE86767E94735980"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" format="dita" scope="local"> type </a> </p> </td> 
  <td class="stentry"> <p>コンテンツタイプのフィルター。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" format="dita" scope="local"> req  </a> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>、 <span class="codeph"> req=props </span>および <span class="codeph"> req=existsの </span> み。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" format="dita" scope="local"> キャッシュ  </a> </p> </td> 
  <td class="stentry"> <p>クライアント側のキャッシュを無効にできます。 </p> </td> 
 </tr> 
</table>

## 基本構文{#section-42103439011540b2b9da3b5eebb442cd}

<table id="simpletable_2F039A5BFA2C4E22B014F42ECBCDA0A2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> リクエスト  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="filepath"> http://  <span class="varname"> server  </span>/is/content[/catalog/  <span class="varname"> item  </span>][?<span class="varname"> 修飾子 </span>]  </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address  </span>[ : <span class="varname"> ポート </span>]  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> カタログ  </span> </span> </p> </td> 
  <td class="stentry"> <p>カタログ識別子。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> item  </span> </span> </p> </td> 
  <td class="stentry"> <p>静的コンテンツ項目ID。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> modifiers  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> command  </span>*[&amp;  <span class="varname"> command  </span>]  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> command  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName  </span>=  <span class="varname"> value  </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName  </span> </span> </p> </td> 
  <td class="stentry"> <p>サポートされているコマンド名の1つ。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>コマンドの値。 </p> </td> 
 </tr> 
</table>

## 静的コンテンツカタログ{#section-91014f17f0d543d7aaf24539b2d7d4b9}

静的コンテンツカタログは画像カタログに似ていますが、サポートされるデータフィールドは少なくなります。

<table id="table_71A565DF5EC94913AD35CB13B0C7A27D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>属性/データ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::Id  </span> </p> </td> 
   <td colname="col2"> <p>この静的コンテンツ項目のカタログレコード識別子です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::Path  </span> </p> </td> 
   <td colname="col2"> <p>このコンテンツ項目のファイルパスです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::Expiration  </span> </p> </td> 
   <td colname="col2"> <p>このコンテンツ項目のTTL。<span class="codeph"> attribute::Expiration </span>は、指定しない場合や空の場合に使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::TimeStamp  </span> </p> </td> 
   <td colname="col2"> <p>ファイル変更のタイムスタンプ<span class="codeph">属性：:CacheValidationPolicy </span>でカタログベースの検証が有効な場合に必須です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::UserData  </span> </p> </td> 
   <td colname="col2"> <p>この静的コンテンツ項目に関連付けられたオプションのメタデータ；<span class="codeph"> req=userdata </span>を使用して、クライアントに提供されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::UserType  </span> </p> </td> 
   <td colname="col2"> <p>オプションのデータ型；は、<span class="codeph"> type=コマンド</span>を使用して、静的コンテンツの要求をフィルタリングするのに使用できます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 静的コンテンツのフィルタリング{#section-4c41bf41ff994910840c1352683d1f37}

このメカニズムは、クライアントがニーズに合ったコンテンツのみを受け取るようにするのに役立ちます。 静的コンテンツに適切な`catalog::UserType`値のタグが付けられている場合、クライアントはリクエストに`type=`コマンドを追加できます。 画像サービングでは、`type=`コマンドによって提供された値を`catalog::UserType`の値と比較し、不一致の場合は、不適切なコンテンツではなくエラーを返します。

## ビデオキャプションファイル{#section-1ad25e10399e43eaa8ecb09b531dbf1a}

ビデオキャプションファイル(WebVTT)、CSSまたは任意のテキストファイルをJSONP形式でカプセル化できます。 JSON応答について以下に説明します。

* WebVTTファイルの場合、応答のMIMEタイプはtext/javascriptです。 JSONが返されない。代わりに、JSONを使用してメソッドを呼び出すJavaScriptが返されます。 IDとハンドラーの両方はオプションです。
* CSSファイルの場合、応答のMIMEタイプはtext/javascriptです。 IDとハンドラーの両方はオプションです。
* デフォルトでは、正しくデコードされるように、UTF-8エンコードが適用されます。 デフォルトのサイズ制限は2 MBです。

また、他の種類の時間指定メタデータにトラックを使用することもできます。 各トラックエレメントのソースデータは、時間指定キューのリストで構成されたテキストファイルです。 キューには、JSONやCSVなどの形式のデータを含めることができます。

JSONP形式について詳しくは、[http://en.wikipedia.org/wiki/JSONP](http://en.wikipedia.org/wiki/JSONP)を参照してください。

JSON形式について詳しくは、[www.json.org](http://www.json.org)を参照してください。

## 関連項目 {#section-7b28631016044a22a3a6762fd64771e9}

[type=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) 、 [req=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)、 [画像カタログの参照](../../is-api/image-serving-api-ref/c-image-catalog-reference/c-image-catalog-reference.md#concept-e23d45ea3abe43119d5144e01c14b0b5)
