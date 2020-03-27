---
description: 'null'
seo-description: 'null'
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Scene7 Image Serving - Image Rendering API
uuid: fd60e5db-9219-41a8-947f-0d497b39e727
translation-type: tm+mt
source-git-commit: 7721cccf3f779f258adcdcf886f7e01111e92be0

---


# TimeStamp{#timestamp}

が設 `attribute::UseLastModified` 定されてい `catalog::TimeStamp` る場合、HTTP応答で値がLast-Modified HTTPヘッダーとして返されます。 静的コンテンツに対しては、最後に変更されたヘッダーが常に返されます(設定されていな `attribute::UseLastModified` い場合も含む)。

画像とSVGコンテンツの場合は、カ `catalog::TimeStamp` タログベースのキャッシュの検証にも使用されます(を参照してく ` [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)`ださい)。

## プロパティ {#section-2298a384b5cb43929542655c5a49beb2}

Java形式の日付/時間値。 1970年1月1日0時からのミリ秒の整数、UTC/GMT、または次のいずれかの形式の日付/時間文字列値を指定できます。

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* *`zzz`*

*`mm`*/ *`dd`*/ *`yyyy`**`hh`*: *`mm`*: *`ss`* GMT *`offset`*

*`hh`* は0 ～ 23の範囲にあります。

*`zzz`* は、「GMT」や「PST」などの3文字または4文字のタイムゾーンコードです。 タイムゾーンコードの夏時間を考慮します。 例えば、太平洋標準時の場合は「PST」、太平洋夏時間の場合は「PDT」)。

*`offset`* は、GMTを基準とした時間単位または時 `hours:minutes`間単位のタイムゾーンのオフセットです。 例えば、「PDT」は「GMT -7」と同じです。

日付/時間の形式を設定した文字列の要素はすべて存在する必要があります。 日付/時間の値の形式が正しくない場合、値は無視され、代わりにカタログファイルの ` *`変更時`*.ini` 間が使用されます。

## 初期設定 {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` フィールドが空か存在しない場合。

## 関連項目 {#section-c42a427aa4794c548408dc4de028d578}

[attribute::TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296), [attribute::UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8), [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
