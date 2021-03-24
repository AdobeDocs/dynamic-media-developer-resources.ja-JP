---
description: ID変換マップ。 汎用の画像IDをロケール固有のIDに変換する際に使用するルールを指定します。
solution: Experience Manager
title: LocaleMap
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 1%

---


# LocaleMap{#localemap}

ID変換マップ。 汎用の画像IDをロケール固有のIDに変換する際に使用するルールを指定します。

`*``*&#42;['|' *`itemitem`*]`

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

`LocaleMap` は、任意の数 `locId` にマップできる `locSuffix`。

空の&#x200B;*`locSuffix`*&#x200B;値を使用できます。 *`locSuffix`* の値は、検索する順序で並べ替える必要があります。最初の一致が返されます。

画像サービングでは、*`locId`*&#x200B;値を検索し、大文字と小文字を区別しないで、要求で指定された`locale=`値と一致するかどうかを確認します。 一致が見つかった場合、最初に関連付けられた&#x200B;*`locSuffix`*&#x200B;値が元のカタログIDに追加されます。 このカタログエントリが存在する場合は使用され、それ以外の場合は次の&#x200B;*`locSuffix`*&#x200B;値が試行されます。 *`locSuffix`*&#x200B;値のいずれもカタログエントリに一致しない場合、画像サービングはエラーまたは初期設定の画像を返します。

空の&#x200B;*`locId`*&#x200B;値は、空および不明な`locale=`文字列と一致します。 これにより、不明なロケールに対するデフォルトのルールを定義できます。

ID変換を有効にすると、画像カタログと静的コンテンツカタログエントリを参照するすべてのIDに適用されます。

## プロパティ {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

1つ以上の項目、区切り |を指定します。各項目は、2つ以上のカンマ区切りの文字列値で構成されます。 *`locId`* と比較 `locale=` されます。大文字と小文字は区別されません。

## 関連項目 {#section-19fba6d5be59439c8bf8ec7513c1a6da}

ローカライゼーションのサポート， [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribute::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
