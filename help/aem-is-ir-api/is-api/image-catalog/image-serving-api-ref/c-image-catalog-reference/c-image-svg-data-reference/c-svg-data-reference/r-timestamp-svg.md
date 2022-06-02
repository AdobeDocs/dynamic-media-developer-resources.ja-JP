---
description: TimeStamp
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e36660bb-d2ec-464c-b578-fe862bca5c50
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 2%

---

# TimeStamp{#timestamp}

If `attribute::UseLastModified` が設定されている場合、 `catalog::TimeStamp` の値は、HTTP 応答で Last-Modified HTTP ヘッダーとして返されます。 静的コンテンツに対しては、常に Last-Modified ヘッダーが返されます ( `attribute::UseLastModified` が設定されていません。

画像およびSVGコンテンツ `catalog::TimeStamp` は、カタログベースのキャッシュ検証にも使用されます ( [attribute::CacheValidationPolicy](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md).

## プロパティ {#section-2298a384b5cb43929542655c5a49beb2}

Java 形式の日時値。 1970 年 1 月 1 日 (UTC/GMT) 午前 0 時からのミリ秒の整数か、次のいずれかの形式を持つ日付/時間文字列値を指定できます。

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* *`zzz`*

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT *`offset`*

*`hh`* は 0 ～ 23 の範囲です。

*`zzz`* は、「GMT」や「PST」などの 3 文字または 4 文字のタイムゾーンコードです。 タイムゾーンコードの夏時間のアカウント。 例えば、太平洋標準時の場合は「PST」、太平洋夏時間の場合は「PDT」)。

*`offset`* は、時間単位のタイムゾーンオフセットです。 `hours:minutes`GMT を基準とした相対値。 例えば、「PDT」は「GMT -7」と同じです。

文字列形式の日付/時刻値の要素はすべて存在する必要があります。 日付/時刻値の形式が正しくない場合、その値は無視され、変更時刻は `*`カタログ`*.ini` ファイルが代わりに使用されます。

## 初期設定 {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` フィールドが空の場合、または存在しない場合。

## 関連項目 {#section-c42a427aa4794c548408dc4de028d578}

[attribute::TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296), [attribute::UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8), [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
