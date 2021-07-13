---
description: TimeStamp
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: e36660bb-d2ec-464c-b578-fe862bca5c50
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 2%

---

# TimeStamp{#timestamp}

`attribute::UseLastModified`が設定されている場合、`catalog::TimeStamp`値がHTTP応答でLast-Modified HTTPヘッダーとして返されます。 `attribute::UseLastModified`が設定されていない場合でも、静的コンテンツに対しては常にLast-Modifiedヘッダーが返されます。

画像とSVGコンテンツの場合、`catalog::TimeStamp`はカタログベースのキャッシュ検証にも使用されます（` [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)`を参照）。

## プロパティ {#section-2298a384b5cb43929542655c5a49beb2}

Java形式の日付/時間値。 1970年1月1日(UTC/GMT)の午前0時からのミリ秒の整数、または次のいずれかの形式を持つ日付/時間文字列値を指定できます。

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*: *`mm`*:  *`ss`* *`zzz`*

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT  *`offset`*

*`hh`* は0 ～ 23の範囲です。

*`zzz`* は、「GMT」や「PST」などの3文字または4文字のタイムゾーンコードです。タイムゾーンコードでの夏時間のアカウント。 例えば、太平洋標準時の場合は「PST」、太平洋夏時間の場合は「PDT」)。

*`offset`* は、GMTに対する、時間単位または時 `hours:minutes`間単位のタイムゾーンオフセットです。例えば、「PDT」は「GMT -7」と同じです。

文字列形式の日付/時間値の要素はすべて存在する必要があります。 日付/時刻の値が正しい形式でない場合は無視され、代わりに`*`catalog`*.ini`ファイルの変更時刻が使用されます。

## 初期設定 {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` を返します。

## 関連項目 {#section-c42a427aa4794c548408dc4de028d578}

[attribute::TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296)、 [attribute::UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8)、 [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
