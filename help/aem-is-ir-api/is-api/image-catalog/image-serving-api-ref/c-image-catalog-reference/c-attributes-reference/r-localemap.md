---
description: ID変換マップ。 汎用の画像IDをロケール固有のIDに変換する際に使用するルールを指定します。
seo-description: ID変換マップ。 汎用の画像IDをロケール固有のIDに変換する際に使用するルールを指定します。
seo-title: LocaleMap
solution: Experience Manager
title: LocaleMap
topic: Scene7 Image Serving - Image Rendering API
uuid: 3609a595-2948-43a4-ba8c-fd1a9ea4e26e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# LocaleMap{#localemap}

ID変換マップ。 汎用の画像IDをロケール固有のIDに変換する際に使用するルールを指定します。

` *`項`*&#42;['|' *`目`*]`

<table id="simpletable_A6DD1A28F8ED4178A8ADDB2F3AEFC402"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 品目</span> </p></td> 
  <td class="stentry"> <p><span class="varname"> locId</span>,<span class="varname"> locSuffix</span>*[','<span class="varname"> locSuffix</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locId</span> </p></td> 
  <td class="stentry"> <p>ロケールID（大文字と小文字は区別されません）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locSuffix</span> </p></td> 
  <td class="stentry"> <p>ロケールサフィックス </p></td> 
 </tr> 
</table>

`LocaleMap` は、任意の数 `locId` のにマップできるを指します `locSuffix`。

Empty *`locSuffix`* values are permitted. *`locSuffix`* の値は、検索する順序で並べ替える必要があります。 最初の一致が返されます。

画像サービングは、値の中 *`locId`* で、要求で指定された値と大文字と小文字が区別さ `locale=` れない一致するものを検索します。 一致が見つかった場合、最初に関連付けら *`locSuffix`* れた値が元のカタログIDに追加されます。 このカタログエントリが存在する場合は使用され、それ以外の場合は次の *`locSuffix`* 値が試行されます。 どの値もカタログエント *`locSuffix`* リと一致しない場合、画像サービングはエラーまたは初期設定の画像を返します。

空の値は、空 *`locId`* の文字列と不明な文字列に一致 `locale=` します。 これにより、不明なロケールのデフォルトのルールを定義できます。

ID変換を有効にすると、画像カタログと静的コンテンツカタログエントリを参照するすべてのIDにID変換が適用されます。

## プロパティ {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

1つ以上の項目(|を参照してください。各項目は、複数のコンマ区切りの文字列値で構成されます。 *`locId`* と比較 `locale=` されます。 大文字と小文字は区別されません。

## 関連項目 {#section-19fba6d5be59439c8bf8ec7513c1a6da}

ローカリゼーションサ [ポート、](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb)locale= [、attribute::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
