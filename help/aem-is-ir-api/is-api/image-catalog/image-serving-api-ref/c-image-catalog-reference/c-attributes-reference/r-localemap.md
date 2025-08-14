---
description: ID 翻訳マップ。 汎用画像 ID をロケール固有の ID に変換するためのルールを指定します。
solution: Experience Manager
title: LocaleMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c1d74154-721b-46cc-9f0b-8dae5647b179
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# LocaleMap{#localemap}

ID 翻訳マップ。 汎用画像 ID をロケール固有の ID に変換するためのルールを指定します。

`*`item`*&#42;['|' *`item`*]`

<table id="simpletable_A6DD1A28F8ED4178A8ADDB2F3AEFC402"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 項目 </span> </p></td> 
  <td class="stentry"> <p><span class="varname"> locId</span>,<span class="varname"> locSuffix</span>*[','<span class="varname"> locSuffix</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locId</span> </p></td> 
  <td class="stentry"> <p>ロケール ID （大文字と小文字を区別しない）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locSuffix</span> </p></td> 
  <td class="stentry"> <p>ロケールサフィックス。 </p></td> 
 </tr> 
</table>

`LocaleMap` は、任意の数の `locId` にマッピングできる `locSuffix` を参照します。

空の *`locSuffix`* 値を使用できます。 値 *`locSuffix`*、検索する順序で並べ替える必要があります。 最初に一致したものが返されます。

画像サービングでは、大文字と小文字を区別せずにリクエストで指定された *`locId`* の値と一致する `locale=` の値を検索します。 一致するものが見つかった場合、最初に関連付けられた *`locSuffix`* 値が元のカタログ ID に付加されます。 このカタログエントリが存在する場合は使用され、存在しない場合は次の *`locSuffix`* 値が試行されます。 カタログエントリに一致する *`locSuffix`* 値がない場合、画像サービングはエラーまたはデフォルト画像を返します。

空の *`locId`* 値は、空の文字列および不明な `locale=` 文字列に一致します。 これにより、不明なロケールにデフォルトのルールを定義できます。

ID 変換を有効にすると、画像カタログおよび静的コンテンツカタログエントリを参照するすべての ID に ID 変換が適用されます。

## プロパティ {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

1 つ以上の項目（で区切られる） |。各項目は、2 つ以上のコンマ区切りの文字列値で構成されます。 *`locId`* と `locale=` が比較されます。 大文字と小文字は区別されません。

## 関連項目 {#section-19fba6d5be59439c8bf8ec7513c1a6da}

ローカリゼーションサポート、[locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb)、[attribute::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
