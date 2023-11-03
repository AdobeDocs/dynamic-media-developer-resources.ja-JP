---
description: ID 変換マップ。 汎用画像 ID をロケール固有の ID に変換する際に使用するルールを指定します。
solution: Experience Manager
title: LocaleMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c1d74154-721b-46cc-9f0b-8dae5647b179
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 1%

---

# LocaleMap{#localemap}

ID 変換マップ。 汎用画像 ID をロケール固有の ID に変換する際に使用するルールを指定します。

`*`項目`*&#42;['|' *`項目`*]`

<table id="simpletable_A6DD1A28F8ED4178A8ADDB2F3AEFC402"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 品目</span> </p></td> 
  <td class="stentry"> <p><span class="varname"> locId</span>,<span class="varname"> locSuffix</span>*[','<span class="varname"> locSuffix</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locId</span> </p></td> 
  <td class="stentry"> <p>ロケール ID（大文字と小文字は区別されません）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locSuffix</span> </p></td> 
  <td class="stentry"> <p>ロケールサフィックス </p></td> 
 </tr> 
</table>

`LocaleMap` は、 `locId` 任意の数の `locSuffix`.

空 *`locSuffix`* の値を指定できます。 *`locSuffix`* 値は、検索順に並べ替える必要があります。 最初の一致が返されます。

画像サービングによる *`locId`* 大文字と小文字を区別しない一致の値 `locale=` リクエストで指定された値。 一致が見つかった場合、最初に関連付けられた *`locSuffix`* の値が元のカタログ ID に追加されます。 このカタログエントリが存在する場合は、そのエントリが使用され、それ以外の場合は次の *`locSuffix`* の値が試行されます。 次のいずれにも該当しない場合、 *`locSuffix`* の値はカタログエントリと一致し、画像サービングはエラーまたはデフォルトの画像を返します。

空の *`locId`* 値が空と不明に一致する `locale=` 文字列。 これにより、不明なロケールに対するデフォルトのルールを定義できます。

ID 変換が有効な場合、画像カタログおよび静的コンテンツカタログエントリを参照するすべての ID に適用されます。

## プロパティ {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

1 つ以上の項目（で区切る） |。各項目は 2 つ以上のコンマ区切りの文字列値で構成されます。 *`locId`* および `locale=` が比較されます。 大文字と小文字は区別されません。

## 関連項目 {#section-19fba6d5be59439c8bf8ec7513c1a6da}

ローカリゼーションサポート [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribute::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
