---
title: 静的（画像以外の）コンテンツの提供
description: 画像サービングを使用して、カタログ内の画像以外のコンテンツを管理し、個別の/is/content コンテキストを介して提供できます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: adc3d972-b02d-40db-992e-acaa06b848ff
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# 静的（画像以外の）コンテンツの提供{#serving-static-non-image-contents}

画像サービングを使用して、カタログ内の画像以外のコンテンツを管理し、個別の/is/content コンテキストを介して提供できます。

この機能を使用すると、各項目の TTL を個別に設定できます。

画像サービングは、次の [!DNL /is/content]:

<table id="simpletable_8A3AB1D1D20F4B6CBE86767E94735980"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" format="dita" scope="local"> type </a> </p> </td> 
  <td class="stentry"> <p>コンテンツタイプフィルター。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" format="dita" scope="local"> req </a> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>, <span class="codeph"> req=props </span>、および <span class="codeph"> req=exists </span> のみ。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" format="dita" scope="local"> キャッシュ </a> </p> </td> 
  <td class="stentry"> <p>クライアント側のキャッシュを無効にすることを許可します。 </p> </td> 
 </tr> 
</table>

## 基本構文 {#section-42103439011540b2b9da3b5eebb442cd}

<table id="simpletable_2F039A5BFA2C4E22B014F42ECBCDA0A2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> リクエスト </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="filepath"> http:// <span class="varname"> server </span>/is/content[/catalog/ <span class="varname"> 項目 </span>][? <span class="varname"> 修飾子 </span>] </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address </span>[ : <span class="varname"> ポート </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> カタログ </span> </span> </p> </td> 
  <td class="stentry"> <p>カタログ識別子。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 項目 </span> </span> </p> </td> 
  <td class="stentry"> <p>静的コンテンツ項目 ID。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 修飾子 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> command </span>*[&amp; <span class="varname"> command </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> command </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span>= <span class="varname"> 値 </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span> </span> </p> </td> 
  <td class="stentry"> <p>サポートされているコマンド名の 1 つ。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 値 </span> </span> </p> </td> 
  <td class="stentry"> <p>コマンドの値。 </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> catalog::Id </span> </p> </td> 
   <td colname="col2"> <p>この静的コンテンツ項目のカタログレコード識別子。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::Path </span> </p> </td> 
   <td colname="col2"> <p>このコンテンツ項目のファイルパス。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::Expiration </span> </p> </td> 
   <td colname="col2"> <p>このコンテンツ項目の TTL。 <span class="codeph"> attribute::Expiration </span> が指定されていない場合、または空の場合は、が使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::TimeStamp </span> </p> </td> 
   <td colname="col2"> <p>ファイル変更のタイムスタンプ。 <span class="codeph"> attribute::CacheValidationPolicy </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::UserData </span> </p> </td> 
   <td colname="col2"> <p>この静的コンテンツ項目に関連付けられたオプションのメタデータ。 <span class="codeph"> req=userdata </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::UserType </span> </p> </td> 
   <td colname="col2"> <p>オプションのデータタイプ。を使用して静的コンテンツの要求を <span class="codeph"> type=コマンド </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 静的コンテンツのフィルタリング {#section-4c41bf41ff994910840c1352683d1f37}

このメカニズムは、クライアントが自分のニーズに合ったコンテンツのみを受け取るようにするのに役立ちます。 静的コンテンツが適切にタグ付けされていると仮定 `catalog::UserType` 値を指定する場合、クライアントは `type=` コマンドを使用して、要求に追加します。 画像サービングでは、 `type=` 値を指示する `catalog::UserType` また、不一致がある場合、は潜在的に不適切なコンテンツの代わりにエラーを返します。

## ビデオキャプションファイル {#section-1ad25e10399e43eaa8ecb09b531dbf1a}

ビデオキャプションファイル (WebVTT)、CSS または任意のテキストファイルを JSONP 形式でカプセル化できます。 JSON 応答を以下に示します。

* WebVTT ファイルの場合、応答の MIME タイプは text/javascript です。 JSON は返されません。代わりに、JSON を使用してメソッドを呼び出す JavaScript が返されます。 ID とハンドラーの両方はオプションです。
* CSS ファイルの場合、応答の MIME タイプは text/javascript です。 ID とハンドラーの両方はオプションです。
* デフォルトでは、UTF-8 エンコーディングが適用され、正しくデコードされます。 デフォルトのサイズ制限は 2 MB です。

他の種類の時間指定メタデータにトラックを使用することもできます。 各トラック要素のソースデータは、時間計測キューのリストで構成されたテキストファイルです。 キューには、JSON や CSV などの形式のデータを含めることができます。

詳しくは、 [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP) を参照してください。

詳しくは、 [www.json.org](https://www.json.org/json-en.html) を参照してください。

## 関連項目 {#section-7b28631016044a22a3a6762fd64771e9}

[type=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) , [req=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [画像カタログ参照](../../is-api/image-serving-api-ref/c-image-catalog-reference/c-image-catalog-reference.md#concept-e23d45ea3abe43119d5144e01c14b0b5)
