---
title: TimeStamp
description: 「attribute::UseLastModified」が設定されている場合、「catalog::TimeStamp」値は、HTTP応答でLast-Modified HTTP ヘッダーとして返されます。 「attribute::UseLastModified」が設定されていない場合でも、静的コンテンツに対してLast-Modified ヘッダーが常に返されます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3c47b14d-b629-474d-952a-b09e1b1162b4
TQID: 'https://experienceleague.adobe.com/wW66KcIShhoLWqgSzWVh5IAGX4pEG4-xUqEZUZ5xckE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 237
ht-degree: 1%

---

# TimeStamp{#timestamp}

`attribute::UseLastModified`が設定されている場合、`catalog::TimeStamp`の値は、HTTP応答でLast-Modified HTTP ヘッダーとして返されます。 `attribute::UseLastModified`が設定されていない場合でも、静的コンテンツに対してLast-Modified ヘッダーが常に返されます。

画像およびSVGのコンテンツでは、`catalog::TimeStamp`はカタログベースのキャッシュ検証にも使用されます（[属性：:CacheValidationPolicy](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md)を参照）。

## プロパティ {#section-2298a384b5cb43929542655c5a49beb2}

Java形式の日時の値。 1970年1月1日の午前0時（UTC/GMT）からのミリ秒数の整数、または次のいずれかの形式の日付/時刻の文字列値を指定できます。

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* *`zzz`*

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT *`offset`*

*`hh`*&#x200B;は0 ～ 23の範囲です。

*`zzz`*&#x200B;は、「GMT」や「PST」などの3文字または4文字のタイムゾーンコードです。 タイムゾーンコードで夏時間を考慮します。 例えば、太平洋標準時の「PST」、太平洋夏時間の「PDT」）。

*`offset`*&#x200B;は、GMTに対する時間または`hours:minutes`のタイムゾーンオフセットです。 例えば、「PDT」は「GMT -7」と同等です。

文字列形式の日付/時刻値のすべての要素が存在する必要があります。 日時の値が正しくフォーマットされていない場合は、無視され、`*` カタログ `*.ini` ファイルの変更時間が代わりに使用されます。

## 初期設定 {#section-0cbf801401ff4857bdda168fd12358af}

フィールドが空であるか存在しない場合、`attribute::TimeStamp`。

## 関連項目 {#section-c42a427aa4794c548408dc4de028d578}

[属性：:TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296)、[属性：:UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8)、[属性：:CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
