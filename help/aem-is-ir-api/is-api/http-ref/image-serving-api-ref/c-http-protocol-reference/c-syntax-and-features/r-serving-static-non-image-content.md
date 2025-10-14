---
description: 静的（非画像）コンテンツの提供
solution: Experience Manager
title: 静的（非画像）コンテンツの提供
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e2c79bdc-5d70-46d9-85f4-ffebd7621944
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# 静的（非画像）コンテンツの提供{#serving-static-non-image-content}

画像サービングは、カタログ内の非画像コンテンツを管理し、別の `context /is/content` ールを介して提供するメカニズムを提供します。 このメカニズムにより、各項目の TTL を個別に設定できます。

## 基本構文 {#section-a986baaca8644d04bcd0ddf781ae916e}

<table id="simpletable_4A6249F0C40747339524323EB0831CE4"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> リクエスト </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> http:// <span class="varname"> server </span>/is/content[/ <span class="varname"> catalog </span>/ <span class="varname"> item </span>][? <span class="varname"> 修飾子 </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address </span>[: <span class="varname"> port </span>] </span> </p> </td> 
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

## コマンドの概要 {#section-61657a0141914053ab12038ad7e91500}

画像サービングは、/is/content で次のコマンドをサポートしています。

<table id="simpletable_1D96BA1AB5394B3C9B91D46617AFC0FA"> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" type="reference" format="dita" scope="local"> type </a> </td> 
  <td class="stentry"> <p>コンテンツタイプフィルター。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req </a> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>、<span class="codeph"> req=props </span>、<span class="codeph"> req=は </span> にのみ存在します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" type="reference" format="dita" scope="local"> cache </a> </td> 
  <td class="stentry"> <p>クライアントサイドのキャッシュを無効にできます。 </p> </td> 
 </tr> 
</table>

## 静的コンテンツカタログ {#section-b2b8f4860fe84e528493ed704c7c5141}

静的コンテンツカタログは、画像カタログに似ていますが、サポートするデータフィールドが少なくなります。

<table id="table_3B111EC3AA1044FB9B659FD54BADDC39"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 属性/データ </b> </th> 
   <th class="entry"> <b> Notes</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::Id </span> </p> </td> 
   <td> <p> この静的コンテンツ項目のカタログ レコード識別子 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::Path </span> </p> </td> 
   <td> <p> このコンテンツ項目のファイルパス </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::Expiration </span> </p> </td> 
   <td> <p> このコンテンツ項目の TTL は、attribute::Expiration が指定されていない場合や空の場合に使用されます </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::TimeStamp </span> </p> </td> 
   <td> <p> ファイル変更タイムスタンプ。属性：:CacheValidationPolicy でカタログベースの検証が有効な場合に必要です </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::UserData </span> </p> </td> 
   <td> <p> この静的コンテンツ項目に関連付けられたオプションのメタデータ。req=userdata を使用してクライアントで使用できます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::UserType </span> </p> </td> 
   <td> <p> オプションのデータタイプ。type= コマンドで静的コンテンツのリクエストをフィルタリングするために使用できます </p> </td> 
  </tr> 
 </tbody> 
</table>

## 静的コンテンツのフィルタリング {#section-896c37cf68bc446eb0766fb378898262}

このメカニズムは、クライアントがニーズに適したコンテンツのみを受け取れるように支援します。 静的コンテンツに適切な `catalog::UserType` 値がタグ付けされている場合、クライアントは `type=` コマンドをリクエストに追加できます。 画像サービングでは、`type=` コマンドで指定された値を `catalog::UserType` の値と比較し、不一致の場合は、不適切な内容の代わりにエラーを返します。

## 関連項目 {#section-91c7b686aacf4d3ca974f35a3fe3d6ec}

[type=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) , [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [&#x200B; 画像カタログ参照 &#x200B;](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
