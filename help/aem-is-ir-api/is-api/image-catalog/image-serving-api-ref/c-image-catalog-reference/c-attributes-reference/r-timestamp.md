---
title: TimeStamp
description: 初期設定の画像変更タイムスタンプ。 カタログの TimeStamp のデフォルト値を提供します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e137f795-e0f7-4b72-b7e8-188e254bbb45
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 1%

---

# TimeStamp{#timestamp}

初期設定の画像変更タイムスタンプ。 catalog::TimeStamp のデフォルト値を指定します。

指定しなかった場合、サーバーはこの変更日時を使用します [!DNL *`catalog`*.ini] ファイル。

## プロパティ {#section-647066e62ce44a84b627fdd0b2f7cfec}

日時の値。 1970 年 1 月 1 日 (UTC/GMT) の午前 0 時からのミリ秒の整数値、または次のいずれかの形式を持つ日付/時間文字列値を指定できます。

日時の値 *`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss zzz`*

日時の値 *`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT *`offset`*

時間の値 *`hh`* は 0 ～ 23 の範囲です。

時間の値 *`zzz`* は、3 文字または 4 文字のタイムゾーンコードです。例： `GMT` または `PST`. 夏時間は、タイムゾーンコードで考慮する必要があります ( 例： `PST` （太平洋標準時の場合）と、 `PDT` （太平洋夏時間用）。

時間の値 *`offset`* は、GMT を基準とした、時間または時間：分単位のタイムゾーンオフセットです。 例： `PDT` はと同じです。 `GMT -7`.

文字列形式の日付/時刻値の要素はすべて存在する必要があります。 日付/時刻値の形式が正しくない場合、その値は無視され、変更時刻は [!DNL *`catalog`*.ini] ファイルが代わりに使用されます。

## 初期設定 {#section-ac465313c97943ed97d41ea852329177}

空の場合や定義されていない場合、サーバーはこの `*`カタログ`*.ini` ファイル。

## 関連項目 {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) , [attribute::UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8), [attribute::CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
