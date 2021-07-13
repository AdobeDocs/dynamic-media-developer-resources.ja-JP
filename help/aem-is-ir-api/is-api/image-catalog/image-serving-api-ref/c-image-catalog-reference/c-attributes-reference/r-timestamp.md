---
description: デフォルトの画像変更タイムスタンプ。 カタログのTimeStampのデフォルト値を指定します。
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: e137f795-e0f7-4b72-b7e8-188e254bbb45
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 2%

---

# TimeStamp{#timestamp}

デフォルトの画像変更タイムスタンプ。 catalog::TimeStampのデフォルト値を指定します。

指定しなかった場合、サーバはこの&#x200B;[!DNL *`catalog`*.ini]ファイルの変更日時を使用します。

## プロパティ {#section-647066e62ce44a84b627fdd0b2f7cfec}

日付/時間値。 1970年1月1日(UTC/GMT)の午前0時からのミリ秒の整数または次のいずれかの形式を持つ日付/時間文字列値を指定できます。

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*: *`mm`*:  *`ss zzz`*

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT  *`offset`*

*`hh`* は0 ～ 23の範囲です。

*`zzz`* は、やなどの3文字または4文字のタイムゾーンコ `GMT` ードで `PST`す。夏時間は、タイムゾーンコード(太平洋標準時の場合は`PST`、太平洋夏時間の場合は`PDT`)。

*`offset`* は、GMTを基準とした、時間または時間：分単位のタイムゾーンオフセットです。例えば、`PDT`は`GMT -7`と同じです。

文字列形式の日付/時間値の要素はすべて存在する必要があります。 日付/時刻の値が正しい形式でない場合は無視され、代わりに&#x200B;[!DNL *`catalog`*.ini]ファイルの変更時刻が使用されます。

## 初期設定 {#section-ac465313c97943ed97d41ea852329177}

空の場合や定義されていない場合、サーバーはこの`*`catalog`*.ini`ファイルのファイル変更時刻を使用します。

## 関連項目 {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) 、 [attribute::UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8)、 [attribute::CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
