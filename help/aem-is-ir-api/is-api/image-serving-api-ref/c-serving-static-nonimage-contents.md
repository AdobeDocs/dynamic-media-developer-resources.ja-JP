---
description: 画像サービングを使用して、カタログ内の画像以外のコンテンツを管理し、個別の/is/contentコンテキストを介して提供できます。
solution: Experience Manager
title: 静的（画像以外）コンテンツの提供
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: adc3d972-b02d-40db-992e-acaa06b848ff
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 0%

---

# 静的（画像以外）コンテンツの提供{#serving-static-non-image-contents}

画像サービングを使用して、カタログ内の画像以外のコンテンツを管理し、個別の/is/contentコンテキストを介して提供できます。

この機能を使用すると、各項目のTTLを個別に設定できます。

画像サービングは、[!DNL /is/content]で次のコマンドをサポートします。

<table id="simpletable_8A3AB1D1D20F4B6CBE86767E94735980"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" format="dita" scope="local"> type </a> </p> </td> 
  <td class="stentry"> <p>コンテンツタイプフィルター。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" format="dita" scope="local"> req  </a> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata  </span>、  <span class="codeph"> req=propsおよび </span>req=existsの <span class="codeph">  </span> み。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" format="dita" scope="local"> キャッシュ  </a> </p> </td> 
  <td class="stentry"> <p>クライアント側のキャッシュを無効にできます。 </p> </td> 
 </tr> 
</table>

## 基本構文 {#section-42103439011540b2b9da3b5eebb442cd}

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
  <td class="stentry"> <p>コマンド値。 </p> </td> 
 </tr> 
</table>

## 静的コンテンツカタログ {#section-91014f17f0d543d7aaf24539b2d7d4b9}

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
   <td colname="col2"> <p>この静的コンテンツ項目のカタログレコード識別子。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::Path  </span> </p> </td> 
   <td colname="col2"> <p>このコンテンツ項目のファイルパス。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::Expiration  </span> </p> </td> 
   <td colname="col2"> <p>このコンテンツ項目のTTL。<span class="codeph"> attribute::Expiration </span>は、指定されていない場合や空の場合に使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::TimeStamp  </span> </p> </td> 
   <td colname="col2"> <p>ファイル変更タイムスタンプ。カタログベースの検証が<span class="codeph">属性：:CacheValidationPolicy </span>で有効な場合に必須です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::UserData  </span> </p> </td> 
   <td colname="col2"> <p>この静的コンテンツ項目に関連付けられたオプションのメタデータ。<span class="codeph"> req=userdata </span>を使用してクライアントが使用できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::UserType  </span> </p> </td> 
   <td colname="col2"> <p>オプションのデータ型を使用して、<span class="codeph"> type=コマンド</span>で静的コンテンツの要求をフィルタリングできます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 静的コンテンツのフィルタリング {#section-4c41bf41ff994910840c1352683d1f37}

このメカニズムは、クライアントがニーズに合ったコンテンツのみを受け取るようにするのに役立ちます。 静的コンテンツに適切な`catalog::UserType`値がタグ付けされている場合、クライアントはリクエストに`type=`コマンドを追加できます。 画像サービングは、`type=`コマンドで指定された値を`catalog::UserType`の値と比較し、不一致の場合は、不適切な可能性があるコンテンツの代わりにエラーを返します。

## ビデオキャプションファイル {#section-1ad25e10399e43eaa8ecb09b531dbf1a}

ビデオキャプションファイル(WebVTT)、CSSまたは任意のテキストファイルをJSONP形式でカプセル化できます。 JSON応答を以下に示します。

* WebVTTファイルの場合、応答のMIMEタイプはtext/javascriptです。 JSONは返されません。代わりに、JSONを使用してメソッドを呼び出すJavaScriptが返されます。 IDとハンドラーの両方はオプションです。
* CSSファイルの場合、応答のMIMEタイプはtext/javascriptです。 IDとハンドラーの両方はオプションです。
* デフォルトでは、UTF-8エンコーディングが適用され、正しくデコードされます。 デフォルトのサイズ制限は2 MBです。

トラックは、他の種類の時間指定メタデータにも使用できます。 各トラック要素のソースデータは、時間指定キューのリストで構成されたテキストファイルです。 キューには、JSONやCSVなどの形式のデータを含めることができます。

JSONP形式について詳しくは、 [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP)を参照してください。

JSON形式について詳しくは、 [www.json.org](https://www.json.org)を参照してください。

## 関連項目 {#section-7b28631016044a22a3a6762fd64771e9}

[type=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) 、  [req=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)、画像カタログ [の参照](../../is-api/image-serving-api-ref/c-image-catalog-reference/c-image-catalog-reference.md#concept-e23d45ea3abe43119d5144e01c14b0b5)
