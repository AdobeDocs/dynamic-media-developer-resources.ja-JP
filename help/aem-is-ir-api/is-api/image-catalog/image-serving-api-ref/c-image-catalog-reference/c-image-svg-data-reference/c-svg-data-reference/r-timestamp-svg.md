---
description: タイムスタンプ
solution: Experience Manager
title: タイムスタンプ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e36660bb-d2ec-464c-b578-fe862bca5c50
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 1%

---

# タイムスタンプ{#timestamp}

`attribute::UseLastModified` が設定されている場合、`catalog::TimeStamp` 値は HTTP 応答で Last-Modified HTTP ヘッダーとして返されます。 静的コンテンツに対しては、Last-Modified ヘッダーが設定されていない場合でも、常に `attribute::UseLastModified` が返されます。

画像およびSVGのコンテンツの場合、`catalog::TimeStamp` はカタログベースのキャッシュ検証にも使用されます（[attribute::CacheValidationPolicy](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md)。

## プロパティ {#section-2298a384b5cb43929542655c5a49beb2}

Java 形式の日付/時刻値。 1970 年 1 月 1 日深夜 10 時からのミリ秒数を表す整数、または日付/時刻を表す文字列値を指定します。次のいずれかの形式を使用できます。

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* *`zzz`*

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT *`offset`*

*`hh`* の範囲は 0 ～ 23 です。

*`zzz`* は、「GMT」や「PST」など、3 文字または 4 文字のタイムゾーンコードです。 タイムゾーンコードの夏時間を考慮します。 例えば、太平洋標準時は「PST」、夏時間は「PDT」です）。

*`offset`* は、GMT を基準とした時間または `hours:minutes` 単位のタイムゾーンオフセットです。 例えば、「PDT」は「GMT -7」と同等です。

文字列形式の日付/時刻値のすべての要素が存在する必要があります。 日付/時刻の値が正しくフォーマットされていない場合、値は無視され、代わりに `*`catalog`*.ini` ファイルの変更時刻が使用されます。

## 初期設定 {#section-0cbf801401ff4857bdda168fd12358af}

フィールドが空か、存在しないかを `attribute::TimeStamp` します。

## 関連項目 {#section-c42a427aa4794c548408dc4de028d578}

[attribute::TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296)、[attribute::UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8)、[attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
