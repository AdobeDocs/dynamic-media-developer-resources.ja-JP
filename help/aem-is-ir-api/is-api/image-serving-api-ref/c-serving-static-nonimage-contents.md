---
title: 静的（画像でない）コンテンツの提供
description: 画像サービングを使用して、カタログ内の画像以外のコンテンツを管理し、別の/is/content コンテキストを介して配信できます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: adc3d972-b02d-40db-992e-acaa06b848ff
TQID: 'https://experienceleague.adobe.com/bC4s5gEY2HaVRGv37BToYmWINn7ZG1JMVp1wSIF60l4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 475
ht-degree: 0%

---

# 静的（画像でない）コンテンツの提供{#serving-static-non-image-contents}

画像サービングを使用して、カタログ内の画像以外のコンテンツを管理し、別の/is/content コンテキストを介して配信できます。

この機能を使用すると、各項目のTTLを個別に設定できます。

画像サービングでは、[!DNL /is/content]で次のコマンドをサポートしています。

<table id="simpletable_8A3AB1D1D20F4B6CBE86767E94735980"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" format="dita" scope="local"> タイプ </a> </p> </td> 
  <td class="stentry"> <p>コンテンツタイプフィルター： </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" format="dita" scope="local">件の質問</a> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>、<span class="codeph"> req=props </span>、<span class="codeph"> req=exists </span>のみ。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" format="dita" scope="local"> キャッシュ </a> </p> </td> 
  <td class="stentry"> <p>クライアントサイドのキャッシュを無効にできます。 </p> </td> 
 </tr> 
</table>

## 基本的な構文 {#section-42103439011540b2b9da3b5eebb442cd}

<table id="simpletable_2F039A5BFA2C4E22B014F42ECBCDA0A2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">要求</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="filepath"> http:// <span class="varname"> サーバー</span>/is/content[/catalog/ <span class="varname">項目</span>][? <span class="varname">個の修飾子</span>] </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> サーバー</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address </span>[ : <span class="varname"> port </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> カタログ </span> </span> </p> </td> 
  <td class="stentry"> <p>カタログ ID: </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">項目</span> </span> </p> </td> 
  <td class="stentry"> <p>静的コンテンツ項目ID。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">修飾子</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> コマンド </span>*[&amp; <span class="varname"> コマンド </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> コマンド </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span>= <span class="varname">値</span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span> </span> </p> </td> 
  <td class="stentry"> <p>サポートされているコマンド名の1つ。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">値</span> </span> </p> </td> 
  <td class="stentry"> <p>コマンド値。 </p> </td> 
 </tr> 
</table>

## 静的コンテンツカタログ {#section-91014f17f0d543d7aaf24539b2d7d4b9}

静的コンテンツカタログは画像カタログと似ていますが、サポートするデータフィールドは少なくなります。

<table id="table_71A565DF5EC94913AD35CB13B0C7A27D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>属性/データ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カタログ：:Id </span> </p> </td> 
   <td colname="col2"> <p>この静的コンテンツ項目のカタログレコード識別子。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カタログ：：パス </span> </p> </td> 
   <td colname="col2"> <p>このコンテンツ項目のファイルパス。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カタログ：：有効期限</span> </p> </td> 
   <td colname="col2"> <p>このコンテンツ項目のTTL。指定されていない場合や空の場合は、<span class="codeph">属性：：有効期限</span>が使用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カタログ：:TimeStamp </span> </p> </td> 
   <td colname="col2"> <p>ファイル変更のタイムスタンプ。カタログベースの検証が<span class="codeph">属性：:CacheValidationPolicy </span>で有効になっている場合に必要です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カタログ：:UserData </span> </p> </td> 
   <td colname="col2"> <p>この静的コンテンツ項目に関連付けられているオプションのメタデータ。クライアントで<span class="codeph"> req=userdata </span>を使用して使用できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カタログ：:UserType </span> </p> </td> 
   <td colname="col2"> <p>オプションのデータ型。静的コンテンツのリクエストを<span class="codeph"> type= コマンド </span>でフィルタリングするために使用できます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 静的コンテンツのフィルタリング {#section-4c41bf41ff994910840c1352683d1f37}

これにより、顧客は自身のニーズに適したコンテンツのみを受け取ることができます。 静的コンテンツが適切な`catalog::UserType`値でタグ付けされていると仮定すると、クライアントはリクエストに`type=` コマンドを追加できます。 Image Servingは、`type=` コマンドで指定された値を`catalog::UserType`の値と比較し、不一致がある場合は、不適切な内容になる可能性がある代わりにエラーを返します。

## ビデオキャプションファイル {#section-1ad25e10399e43eaa8ecb09b531dbf1a}

ビデオキャプションファイル（WebVTT）、CSS、または任意のテキストファイルをJSONP形式でカプセル化できます。 JSON応答については以下で説明します。

* WebVTT ファイルの場合、応答のMIME タイプはtext/javascriptです。 JSONは返されません。代わりに、JSONを使用してメソッドを呼び出すJavaScriptが返されます。 IDとハンドラーの両方はオプションです。
* CSS ファイルの場合、応答のMIME タイプはtext/javascriptです。 IDとハンドラーの両方はオプションです。
* デフォルトでは、UTF-8 エンコーディングが適用され、正しくデコードされます。 デフォルトのサイズ制限は2 MBです。

他の種類のタイムメタデータにトラックを使用することもできます。 各トラックエレメントのソースデータは、タイムキューのリストで構成されるテキストファイルです。 キューには、JSONやCSVなどの形式でデータを含めることができます。

JSONP形式について詳しくは、[https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP)を参照してください。

JSON形式について詳しくは、[www.json.org](https://www.json.org/json-en.html)を参照してください。

## 関連項目 {#section-7b28631016044a22a3a6762fd64771e9}

[type=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb)、[req=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)、[画像カタログ参照](../../is-api/image-serving-api-ref/c-image-catalog-reference/c-image-catalog-reference.md#concept-e23d45ea3abe43119d5144e01c14b0b5)
