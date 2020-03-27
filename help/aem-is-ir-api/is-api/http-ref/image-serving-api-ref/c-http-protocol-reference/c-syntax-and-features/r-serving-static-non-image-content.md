---
description: 'null'
seo-description: 'null'
seo-title: 静的（画像以外）コンテンツの提供
solution: Experience Manager
title: 静的（画像以外）コンテンツの提供
topic: Scene7 Image Serving - Image Rendering API
uuid: 4ec483fe-68a4-4ae2-b5ce-730229a9bc15
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 静的（画像以外）コンテンツの提供{#serving-static-non-image-content}

画像サービングは、カタログ内の画像以外のコンテンツを管理し、別のメカニズムを介して提供するメカニズムを提供しま `context /is/content`す。 このメカニズムを使用すると、各項目のTTLを個別に設定できます。

## 基本構文 {#section-a986baaca8644d04bcd0ddf781ae916e}

<table id="simpletable_4A6249F0C40747339524323EB0831CE4"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 要 </span> 求 </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> http:// <span class="varname"> server </span>/is/content[/ <span class="varname"> catalog </span>/ <span class="varname"></span>item ][? <span class="varname"> 修飾子 </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> サーバ </span> ー </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address </span>[: <span class="varname"> ポ </span>ート] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> カタ </span> ログ </span> </p> </td> 
  <td class="stentry"> <p>カタログ識別子。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 項 </span> 目 </span> </p> </td> 
  <td class="stentry"> <p>静的コンテンツ項目ID。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 修飾 </span> 子 </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> コマ </span>ンド*[&amp; <span class="varname"> command </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 指 </span> 令 </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span>= <span class="varname"> value </span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span></span> </p> </td> 
  <td class="stentry"> <p>サポートされているコマンド名の1つ。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 価 </span> 値 </span> </p> </td> 
  <td class="stentry"> <p>コマンドの値。 </p> </td> 
 </tr> 
</table>

## コマンドの概要 {#section-61657a0141914053ab12038ad7e91500}

画像サービングは、/is/contentで次のコマンドをサポートします。

<table id="simpletable_1D96BA1AB5394B3C9B91D46617AFC0FA"> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" type="reference" format="dita" scope="local"> type </a> </td> 
  <td class="stentry"> <p>コンテンツタイプのフィルタ。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req </a> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata、 </span>req=propsお <span class="codeph"> よび </span>req=existsの <span class="codeph"></span> み。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" type="reference" format="dita" scope="local"> キャッシュ </a> </td> 
  <td class="stentry"> <p>クライアント側のキャッシュを無効にできます。 </p> </td> 
 </tr> 
</table>

## 静的コンテンツカタログ {#section-b2b8f4860fe84e528493ed704c7c5141}

静的コンテンツカタログは画像カタログに似ていますが、サポートされるデータフィールドの数は少なくなります。

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
   <td> <p> このコンテンツアイテムのファイルパス </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::Expiration </span> </p> </td> 
   <td> <p> このコンテンツ項目のTTL。attribute::Expirationが使用される（指定されていない場合または空の場合） </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::TimeStamp </span> </p> </td> 
   <td> <p> ファイル変更タイムスタンプattribute::CacheValidationPolicyを使用してカタログベースの検証が有効な場合に必須 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::UserData </span> </p> </td> 
   <td> <p> この静的コンテンツアイテムに関連付けられたオプションのメタデータ。req=userdataを使用してクライアントが使用可能 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::UserType </span> </p> </td> 
   <td> <p> オプションのデータ型。type=コマンドを使用して静的コンテンツの要求をフィルタリングする </p> </td> 
  </tr> 
 </tbody> 
</table>

## 静的コンテンツのフィルタリング {#section-896c37cf68bc446eb0766fb378898262}

このメカニズムは、クライアントがニーズに合ったコンテンツのみを受け取るようにするのに役立ちます。 静的コンテンツが適切な値でタグ付けされてい `catalog::UserType`ると仮定して、クライアントはリクエストにコ `type=` マンドを追加できます。 画像サービングは、コマンドで指定された値 `type=` との値を比較し、不一致が発生し `catalog::UserType` た場合は、不適切な内容の可能性があるのではなく、エラーを返します。

## 関連項目 {#section-91c7b686aacf4d3ca974f35a3fe3d6ec}

[type=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) , [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Image Catalog Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
