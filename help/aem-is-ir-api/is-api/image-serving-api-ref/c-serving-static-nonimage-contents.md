---
title: 静的（非画像）コンテンツの提供
description: 画像サービングを使用して、カタログ内の非画像コンテンツを管理し、別の/is/content コンテキストを介して提供できます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: adc3d972-b02d-40db-992e-acaa06b848ff
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# 静的（非画像）コンテンツの提供{#serving-static-non-image-contents}

画像サービングを使用して、カタログ内の非画像コンテンツを管理し、別の/is/content コンテキストを介して提供できます。

この機能を使用すると、各項目の TTL を個別に設定できます。

画像サービングでは、[!DNL /is/content] で次のコマンドをサポートしています。

<table id="simpletable_8A3AB1D1D20F4B6CBE86767E94735980"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" format="dita" scope="local"> type </a> </p> </td> 
  <td class="stentry"> <p>コンテンツタイプフィルター。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" format="dita" scope="local"> req </a> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>、<span class="codeph"> req=props </span>、<span class="codeph"> req=は </span> にのみ存在します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" format="dita" scope="local"> cache </a> </p> </td> 
  <td class="stentry"> <p>クライアントサイドのキャッシュを無効にできます。 </p> </td> 
 </tr> 
</table>

## 基本構文 {#section-42103439011540b2b9da3b5eebb442cd}

<table id="simpletable_2F039A5BFA2C4E22B014F42ECBCDA0A2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> リクエスト </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="filepath"> http:// <span class="varname"> server </span>/is/content[/catalog/ <span class="varname"> item </span>][? <span class="varname"> 修飾子 </span>] </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address </span>[ : <span class="varname"> port </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> catalog </span> </span> </p> </td> 
  <td class="stentry"> <p>カタログ識別子。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> item </span> </span> </p> </td> 
  <td class="stentry"> <p>静的コンテンツ項目 ID。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 修飾子 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> コマンド </span>*[&amp; <span class="varname"> コマンド </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> command </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span>= <span class="varname"> value </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span> </span> </p> </td> 
  <td class="stentry"> <p>サポートされるコマンド名の 1 つ。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 値 </span> </span> </p> </td> 
  <td class="stentry"> <p>コマンド値。 </p> </td> 
 </tr> 
</table>

## 静的コンテンツカタログ {#section-91014f17f0d543d7aaf24539b2d7d4b9}

静的コンテンツカタログは、画像カタログに似ていますが、サポートするデータフィールドが少なくなります。

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
   <td colname="col2"> <p>このコンテンツ項目の TTL は、属性：:Expiration <span class="codeph"> が指定されていない場合 </span>、または空の場合に使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::TimeStamp </span> </p> </td> 
   <td colname="col2"> <p>ファイル変更のタイムスタンプ。属性：:CacheValidationPolicy <span class="codeph"> でカタログベースの検証が有効 </span> なっている場合に必要です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::UserData </span> </p> </td> 
   <td colname="col2"> <p>この静的コンテンツ項目に関連付けられたオプションのメタデータです。req=userdata <span class="codeph"> を持つクライアント </span> 使用できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::UserType </span> </p> </td> 
   <td colname="col2"> <p>オプションのデータタイプ。<span class="codeph"> type= コマンド </span> を使用して静的コンテンツのリクエストをフィルタリングするために使用できます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 静的コンテンツのフィルタリング {#section-4c41bf41ff994910840c1352683d1f37}

このメカニズムは、クライアントがニーズに適したコンテンツのみを受け取れるように支援します。 静的コンテンツに適切な `catalog::UserType` 値がタグ付けされている場合、クライアントは `type=` コマンドをリクエストに追加できます。 画像サービングでは、`type=` コマンドで指定された値が `catalog::UserType` の値と比較され、不一致がある場合、不適切な内容の代わりにエラーが返されます。

## ビデオキャプションファイル {#section-1ad25e10399e43eaa8ecb09b531dbf1a}

ビデオキャプションファイル（WebVTT）、CSS、または任意のテキストファイルを JSONP 形式でカプセル化できます。 JSON 応答については以下で説明します。

* WebVTT ファイルの場合、応答の MIME タイプは text/javascript です。 JSON は返されません。代わりに、JSON を含むメソッドを呼び出すJavaScriptが返されます。 ID とハンドラーは両方ともオプションです。
* CSS ファイルの場合、応答の MIME タイプは text/javascript です。 ID とハンドラーは両方ともオプションです。
* デフォルトでは、正しくデコードされるように UTF-8 エンコーディングが適用されます。 デフォルトのサイズ制限は 2 MB です。

また、他の種類のタイムドメタデータ用のトラックを使用することもできます。 各トラック要素のソースデータは、タイムドキューのリストで構成されるテキストファイルです。 キューには、JSON や CSV などの形式のデータを含めることができます。

JSONP 形式について詳しくは、[https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP) を参照してください。

JSON 形式について詳しくは、[www.json.org](https://www.json.org/json-en.html) を参照してください。

## 関連項目 {#section-7b28631016044a22a3a6762fd64771e9}

[type=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) , [req=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [&#x200B; 画像カタログ参照 &#x200B;](../../is-api/image-serving-api-ref/c-image-catalog-reference/c-image-catalog-reference.md#concept-e23d45ea3abe43119d5144e01c14b0b5)
