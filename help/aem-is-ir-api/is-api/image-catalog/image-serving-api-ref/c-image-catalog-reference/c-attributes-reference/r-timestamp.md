---
description: 初期設定の画像変更タイムスタンプ。 カタログのTimeStampのデフォルト値を指定します。
seo-description: 初期設定の画像変更タイムスタンプ。 カタログのTimeStampのデフォルト値を指定します。
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Scene7 Image Serving - Image Rendering API
uuid: 0670e53a-ad7d-46cf-8e18-4c52a766df6f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# TimeStamp{#timestamp}

初期設定の画像変更タイムスタンプ。 catalog::TimeStampのデフォルト値を指定します。

指定しなかった場合、サーバはこの [!DNL *`catalog`*.iniファイルの変更日時を使用します] 。

## プロパティ {#section-647066e62ce44a84b627fdd0b2f7cfec}

日付/時間の値。 1970年1月1日0時(UTC/GMT)からのミリ秒の整数または日時文字列値で、次のいずれかの形式を使用できます。

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss zzz`*

*`mm`*/ *`dd`*/ *`yyyy`**`hh`*: *`mm`*: *`ss`* GMT *`offset`*

*`hh`* は0 ～ 23の範囲です。

*`zzz`* は、またはなどの3文字または4文字のタイムゾーンコ `GMT` ードで `PST`す。 夏時間は、タイムゾーンコードで計上する必要があります(太平洋標準時 `PST` 間の場合と太平洋夏時間の `PDT` 場合など)。

*`offset`* は、GMTを基準とした時間または時間：分単位のタイムゾーンのオフセットです。 例えば、はと同 `PDT` 等の値です `GMT -7`。

日付/時間の形式を設定した文字列の要素はすべて存在する必要があります。 日付/時刻値の形式が正しくない場合は無視され、 [!DNL *`catalog`*.iniファイルの変更時刻が代わりに使用されます] 。

## 初期設定 {#section-ac465313c97943ed97d41ea852329177}

空の場合、または定義されていない場合、サーバはこのカタログファイルのファイル変更時刻を ` *`使用し`*.ini` ます。

## 関連項目 {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) 、 [attribute::UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8)、 [attribute::CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
