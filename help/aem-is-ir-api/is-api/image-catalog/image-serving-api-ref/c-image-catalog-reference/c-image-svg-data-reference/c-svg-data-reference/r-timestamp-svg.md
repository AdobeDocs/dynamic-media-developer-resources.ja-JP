---
description: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Scene7 Image Serving - Image Rendering API
uuid: 9ce5e42e-573a-4e1c-97d4-98888e16ca56
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 2%

---


# TimeStamp{#timestamp}

`attribute::UseLastModified`が設定されている場合、`catalog::TimeStamp`値はHTTP応答内で最終変更HTTPヘッダーとして返されます。 `attribute::UseLastModified`が設定されていない場合でも、静的コンテンツの場合は常に「最終変更日」ヘッダが返されます。

画像とSVGコンテンツの場合は、`catalog::TimeStamp`はカタログベースのキャッシュ検証にも使用されます（` [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)`を参照）。

## プロパティ {#section-2298a384b5cb43929542655c5a49beb2}

Java形式の日付/時間値。 値は、午前0時からのミリ秒の整数、1970年1月1日(UTC/GMT)、または日付/時間文字列値で、次のいずれかの形式になります。

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*: *`mm`*:  *`ss`* *`zzz`*

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT  *`offset`*

*`hh`* は0 ～ 23の範囲にあります。

*`zzz`* は、「GMT」や「PST」などの3文字または4文字のタイムゾーンコードです。タイムゾーンコードでの夏時間のアカウント。 例えば、太平洋標準時の場合は「PST」、太平洋夏時間の場合は「PDT」)。

*`offset`* は、GMTを基準とした、時間単位または時 `hours:minutes`間単位のタイムゾーンオフセットです。例えば、「PDT」は「GMT -7」と同じです。

日付/時間形式の文字列値の要素はすべて存在する必要があります。 日付/時刻値の形式が正しくない場合、この値は無視され、代わりに` *`カタログ`*.ini`ファイルの変更時刻が使用されます。

## 初期設定 {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` フィールドが空の場合、または存在しない場合。

## 関連項目 {#section-c42a427aa4794c548408dc4de028d578}

[attribute::TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296),  [attribute::UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8),  [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
