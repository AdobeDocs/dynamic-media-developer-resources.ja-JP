---
description: 静的（画像以外の）コンテンツの提供
solution: Experience Manager
title: 静的（画像以外の）コンテンツの提供
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e2c79bdc-5d70-46d9-85f4-ffebd7621944
TQID: 'https://experienceleague.adobe.com/fWwGD0B2IS6rd7Ls6rEb2RzH82e-lFHS2WUBrNGe7QY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 291
ht-degree: 0%

---

# 静的（画像以外の）コンテンツの提供{#serving-static-non-image-content}

画像サービングは、カタログ内の画像以外のコンテンツを管理し、別の`context /is/content`を介して提供するメカニズムを提供します。 このメカニズムにより、各項目のTTLを個別に設定できます。

## 基本的な構文 {#section-a986baaca8644d04bcd0ddf781ae916e}

<table id="simpletable_4A6249F0C40747339524323EB0831CE4"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">要求</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> http:// <span class="varname"> サーバー</span>/is/content[/ <span class="varname"> カタログ </span>/ <span class="varname">項目</span>][? <span class="varname">個の修飾子</span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> サーバー</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address </span>[: <span class="varname"> port </span>] </span> </p> </td> 
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

## コマンドの概要 {#section-61657a0141914053ab12038ad7e91500}

画像サービングでは、/is/contentで次のコマンドをサポートしています。

<table id="simpletable_1D96BA1AB5394B3C9B91D46617AFC0FA"> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" type="reference" format="dita" scope="local"> タイプ </a> </td> 
  <td class="stentry"> <p>コンテンツタイプフィルター： </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local">件の質問</a> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>、<span class="codeph"> req=props </span>、<span class="codeph"> req=exists </span>のみ。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" type="reference" format="dita" scope="local"> キャッシュ </a> </td> 
  <td class="stentry"> <p>クライアントサイドのキャッシュを無効にできます。 </p> </td> 
 </tr> 
</table>

## 静的コンテンツカタログ {#section-b2b8f4860fe84e528493ed704c7c5141}

静的コンテンツカタログは画像カタログと似ていますが、サポートするデータフィールドは少なくなります。

<table id="table_3B111EC3AA1044FB9B659FD54BADDC39"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>属性/データ </b> </th> 
   <th class="entry"> <b>件のメモ </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> カタログ：:Id </span> </p> </td> 
   <td> <p> この静的コンテンツ項目のカタログレコード識別子 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> カタログ：：パス </span> </p> </td> 
   <td> <p> このコンテンツ項目のファイルパス </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> カタログ：：有効期限</span> </p> </td> 
   <td> <p> このコンテンツ項目のTTL。指定されていない場合や空の場合は、属性：:Expirationが使用されます </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> カタログ：:TimeStamp </span> </p> </td> 
   <td> <p> ファイル変更のタイムスタンプ。カタログベースの検証が属性：:CacheValidationPolicyで有効になっている場合に必要です。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> カタログ：:UserData </span> </p> </td> 
   <td> <p> この静的コンテンツ項目に関連付けられているオプションのメタデータ。req=userdataを使用してクライアントで使用できます </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> カタログ：:UserType </span> </p> </td> 
   <td> <p> オプションのデータタイプ。type= コマンドを使用して、静的コンテンツのリクエストをフィルタリングするために使用できます </p> </td> 
  </tr> 
 </tbody> 
</table>

## 静的コンテンツのフィルタリング {#section-896c37cf68bc446eb0766fb378898262}

これにより、顧客は自身のニーズに適したコンテンツのみを受け取ることができます。 静的コンテンツに適切な`catalog::UserType`値がタグ付けされていると仮定すると、クライアントはリクエストに`type=` コマンドを追加できます。 画像サービングは、`type=` コマンドで指定された値を`catalog::UserType`の値と比較し、不一致の場合は、不適切なコンテンツが発生する可能性がある代わりにエラーを返します。

## 関連項目 {#section-91c7b686aacf4d3ca974f35a3fe3d6ec}

[type=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb)、[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)、[画像カタログ参照](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
