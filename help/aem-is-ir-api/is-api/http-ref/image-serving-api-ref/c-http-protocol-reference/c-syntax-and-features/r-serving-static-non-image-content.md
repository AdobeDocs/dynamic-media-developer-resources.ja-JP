---
description: 静的（画像以外の）コンテンツの提供
solution: Experience Manager
title: 静的（画像以外の）コンテンツの提供
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e2c79bdc-5d70-46d9-85f4-ffebd7621944
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 1%

---

# 静的（画像以外の）コンテンツの提供{#serving-static-non-image-content}

画像サービングは、カタログ内の画像以外のコンテンツを管理し、それを個別の方法で提供するメカニズムを提供します `context /is/content`. このメカニズムでは、各項目の TTL を個別に設定できます。

## 基本構文 {#section-a986baaca8644d04bcd0ddf781ae916e}

<table id="simpletable_4A6249F0C40747339524323EB0831CE4"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> リクエスト </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> http:// <span class="varname"> server </span>/is/content[/ <span class="varname"> カタログ </span>/ <span class="varname"> 項目 </span>][? <span class="varname"> 修飾子 </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address </span>[: <span class="varname"> ポート </span>] </span> </p> </td> 
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

## コマンドの概要 {#section-61657a0141914053ab12038ad7e91500}

画像サービングは、/is/content で次のコマンドをサポートします。

<table id="simpletable_1D96BA1AB5394B3C9B91D46617AFC0FA"> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" type="reference" format="dita" scope="local"> type </a> </td> 
  <td class="stentry"> <p>コンテンツタイプフィルター。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req </a> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>, <span class="codeph"> req=props </span>、および <span class="codeph"> req=exists </span> のみ。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" type="reference" format="dita" scope="local"> キャッシュ </a> </td> 
  <td class="stentry"> <p>クライアント側のキャッシュを無効にすることを許可します。 </p> </td> 
 </tr> 
</table>

## 静的コンテンツカタログ {#section-b2b8f4860fe84e528493ed704c7c5141}

静的コンテンツカタログは画像カタログに似ていますが、サポートされるデータフィールドは少なくなります。

<table id="table_3B111EC3AA1044FB9B659FD54BADDC39"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 属性/データ</b> </th> 
   <th class="entry"> <b> 説明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::Id </span> </p> </td> 
   <td> <p> この静的コンテンツ項目のカタログレコード識別子 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::Path </span> </p> </td> 
   <td> <p> このコンテンツ項目のファイルパス </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::Expiration </span> </p> </td> 
   <td> <p> このコンテンツ項目の TTL。指定されていない場合、または空の場合は attribute::Expiration が使用されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::TimeStamp </span> </p> </td> 
   <td> <p> ファイル変更タイムスタンプ。属性：:CacheValidationPolicy でカタログベースの検証が有効な場合に必要です。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::UserData </span> </p> </td> 
   <td> <p> この静的コンテンツ項目に関連付けられたオプションのメタデータ。req=userdata を使用してクライアントが使用できます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::UserType </span> </p> </td> 
   <td> <p> オプションのデータ型です。type=コマンドを使用して静的コンテンツの要求をフィルタリングするために使用できます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 静的コンテンツのフィルタリング {#section-896c37cf68bc446eb0766fb378898262}

このメカニズムは、クライアントが自分のニーズに合ったコンテンツのみを受け取るようにするのに役立ちます。 静的コンテンツが適切にタグ付けされていると仮定 `catalog::UserType`値を指定する場合、クライアントは `type=` コマンドを使用して、要求に追加します。 画像サービングでは、 `type=` 値を指示する `catalog::UserType` また、不一致の場合、不適切な可能性のあるコンテンツの代わりにエラーを返します。

## 関連項目 {#section-91c7b686aacf4d3ca974f35a3fe3d6ec}

[type=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) , [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [画像カタログ参照](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
