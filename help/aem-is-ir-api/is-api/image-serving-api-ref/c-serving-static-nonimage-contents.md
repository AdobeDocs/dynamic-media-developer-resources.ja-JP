---
description: 画像サービングを使用して、カタログ内の画像以外のコンテンツを管理し、個別の/is/contentコンテキストを介して提供できます。
seo-description: 画像サービングを使用して、カタログ内の画像以外のコンテンツを管理し、個別の/is/contentコンテキストを介して提供できます。
seo-title: 静的（画像以外）コンテンツの提供
solution: Experience Manager
title: 静的（画像以外）コンテンツの提供
topic: Scene7 Image Serving - Image Rendering API
uuid: bdb1383a-e02d-499f-be79-4a6dc501705c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 静的（画像以外）コンテンツの提供{#serving-static-non-image-contents}

画像サービングを使用して、カタログ内の画像以外のコンテンツを管理し、個別の/is/contentコンテキストを介して提供できます。

この機能を使用すると、各項目のTTLを個別に設定できます。

画像サービングは、次のコマンドをサポートしていま [!DNL /is/content]す。

<table id="simpletable_8A3AB1D1D20F4B6CBE86767E94735980"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" format="dita" scope="local"> type </a> </p> </td> 
  <td class="stentry"> <p>コンテンツタイプのフィルタ。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" format="dita" scope="local"> req </a> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata、 </span>req=propsお <span class="codeph"> よび </span>req=existsの <span class="codeph"></span> み。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" format="dita" scope="local"> キャッシュ </a> </p> </td> 
  <td class="stentry"> <p>クライアント側のキャッシュを無効にできます。 </p> </td> 
 </tr> 
</table>

## 基本構文 {#section-42103439011540b2b9da3b5eebb442cd}

<table id="simpletable_2F039A5BFA2C4E22B014F42ECBCDA0A2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 要 </span> 求 </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="filepath"> http:// <span class="varname"></span>server <span class="varname"> /is/content[/catalog/ </span>item ][? <span class="varname"> 修飾子 </span>] </span> [ </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> サーバ </span> ー </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address </span>[ : <span class="varname"> ポ </span>ート] </span> </p> </td> 
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

## 静的コンテンツカタログ {#section-91014f17f0d543d7aaf24539b2d7d4b9}

静的コンテンツカタログは画像カタログに似ていますが、サポートされるデータフィールドの数は少なくなります。

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
   <td colname="col2"> <p>この静的コンテンツアイテムのカタログレコード識別子。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::Path </span> </p> </td> 
   <td colname="col2"> <p>このコンテンツアイテムのファイルパス。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::Expiration </span> </p> </td> 
   <td colname="col2"> <p>このコンテンツ項目のTTL。 <span class="codeph"> attribute::Expirationが使用され </span> る（指定されていない場合または空の場合）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::TimeStamp </span> </p> </td> 
   <td colname="col2"> <p>ファイル変更タイムスタンプattribute::CacheValidationPolicyを使用してカタログベースの検証が有効にな <span class="codeph"> っている場合は必須で </span>す。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::UserData </span> </p> </td> 
   <td colname="col2"> <p>この静的コンテンツアイテムに関連付けられたオプションのメタデータ。を <span class="codeph"> req=userdataでクライアントが使用できるようにしま </span>す。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::UserType </span> </p> </td> 
   <td colname="col2"> <p>オプションのデータ型。は、type=コマンドを使用して静的コンテンツの要求をフィルタリ <span class="codeph"> ングする場合に使用しま </span>す。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 静的コンテンツのフィルタリング {#section-4c41bf41ff994910840c1352683d1f37}

このメカニズムは、クライアントがニーズに合ったコンテンツのみを受け取るようにするのに役立ちます。 静的コンテンツが適切な値でタグ付けされてい `catalog::UserType` ると仮定して、クライアントはリクエストにコ `type=` マンドを追加できます。 画像サービングでは、コマンドで指定された値 `type=` との値を比較し、不一致が発生し `catalog::UserType` た場合は、不適切なコンテンツの可能性があるのではなく、エラーを返します。

## ビデオキャプションファイル {#section-1ad25e10399e43eaa8ecb09b531dbf1a}

ビデオキャプションファイル(WebVTT)、CSSまたは任意のテキストファイルをJSONP形式でカプセル化できます。 JSON応答について以下に説明します。

* WebVTTファイルの場合、応答のMIMEタイプはtext/javascriptです。 JSONが返されない。代わりに、JSONを使用してメソッドを呼び出すJavaScriptが返されます。 IDとハンドラーの両方はオプションです。
* CSSファイルの場合、応答のMIMEタイプはtext/javascriptです。 IDとハンドラーの両方はオプションです。
* デフォルトでは、UTF-8エンコーディングが適用され、正しくデコードされます。 デフォルトのサイズ制限は2 MBです。

また、他の種類の時間指定メタデータにトラックを使用することもできます。 各トラック要素のソースデータは、時間指定キューのリストで構成されたテキストファイルです。 キューには、JSONやCSVなどの形式のデータを含めることができます。

JSONP形式につ [いて詳しくは](http://en.wikipedia.org/wiki/JSONP) 、http://en.wikipedia.org/wiki/JSONPを参照してください。

JSON形式につ [いて詳しくは](http://www.json.org) 、www.json.orgを参照してください。

## 関連項目 {#section-7b28631016044a22a3a6762fd64771e9}

[type=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) , [req=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Image Catalog Reference](../../is-api/image-serving-api-ref/c-image-catalog-reference/c-image-catalog-reference.md#concept-e23d45ea3abe43119d5144e01c14b0b5)
