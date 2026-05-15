---
description: ID翻訳マップ： 汎用画像IDをロケール固有のIDに変換するために使用するルールを指定します。
solution: Experience Manager
title: LocaleMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c1d74154-721b-46cc-9f0b-8dae5647b179
TQID: 'https://experienceleague.adobe.com/LqHo03WC7EWKP7jt4l1X6kJffXcOQSd8unCxbdjOig4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 213
ht-degree: 0%

---

# LocaleMap{#localemap}

ID翻訳マップ： 汎用画像IDをロケール固有のIDに変換するために使用するルールを指定します。

`*`項目`*&#42;['|' *`項目`*]`

<table id="simpletable_A6DD1A28F8ED4178A8ADDB2F3AEFC402"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">項目</span> </p></td> 
  <td class="stentry"> <p><span class="varname"> locId</span>,<span class="varname"> locSuffix</span>*[','<span class="varname"> locSuffix</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locId</span> </p></td> 
  <td class="stentry"> <p>ロケール ID （大文字と小文字は区別されません）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locSuffix</span> </p></td> 
  <td class="stentry"> <p>ロケールサフィックス。 </p></td> 
 </tr> 
</table>

`LocaleMap`は、任意の数の`locSuffix`にマッピングできる`locId`を指します。

空の&#x200B;*`locSuffix`*&#x200B;値を使用できます。 *`locSuffix`*&#x200B;個の値は、検索する順序で並べ替える必要があります。 最初の一致が返されます。

画像サービングは、リクエストで指定された`locale=`値と大文字と小文字を区別しない一致を&#x200B;*`locId`*&#x200B;値で検索します。 一致が見つかった場合、最初に関連付けられた&#x200B;*`locSuffix`*&#x200B;値が元のカタログ IDに追加されます。 このカタログエントリが存在する場合は使用されます。そうでない場合は、次の&#x200B;*`locSuffix`*&#x200B;値が試されます。 *`locSuffix`*&#x200B;の値のいずれもカタログ エントリと一致しない場合、Image Servingはエラーまたはデフォルトの画像を返します。

空の&#x200B;*`locId`*&#x200B;値は、空の`locale=`文字列と不明な文字列と一致します。 これにより、不明なロケールに対するデフォルトのルールを定義できます。

ID翻訳を有効にすると、画像カタログと静的コンテンツカタログエントリを参照するすべてのIDに適用されます。

## プロパティ {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

1つ以上の項目を|で区切り、各項目が2つ以上のコンマ区切りの文字列値で構成されます。 *`locId`*&#x200B;と`locale=`が比較されます。 大文字と小文字を区別しない。

## 関連項目 {#section-19fba6d5be59439c8bf8ec7513c1a6da}

ローカライゼーションのサポート、[locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb)、[属性：:LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
