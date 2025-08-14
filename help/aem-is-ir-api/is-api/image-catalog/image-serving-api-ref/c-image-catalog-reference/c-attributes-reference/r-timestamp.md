---
title: タイムスタンプ
description: デフォルトの画像変更タイムスタンプ。 カタログのタイムスタンプのデフォルト値を提供します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e137f795-e0f7-4b72-b7e8-188e254bbb45
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 1%

---

# タイムスタンプ{#timestamp}

デフォルトの画像変更タイムスタンプ。 catalog::TimeStamp にデフォルト値を指定します。

指定しない場合、サーバーはこの [!DNL *`catalog`*.ini] ファイルの変更日時を使用します。

## プロパティ {#section-647066e62ce44a84b627fdd0b2f7cfec}

日付/時刻の値。 1970 年 1 月 1 日深夜 0 時からのミリ秒数の整数、1970 年 1 月 1 日の UTC/GMT、または日付/時刻の文字列値を次のいずれかの形式で指定します。

日付/時刻の値 *`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss zzz`*

日時値 *`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT *`offset`*

時間値 *`hh`* は 0～23 の範囲です。

時間値 *`zzz`* は、`GMT` や `PST` など、3 文字または 4 文字のタイムゾーンコードです。 夏時間は、タイムゾーンコードで考慮する必要があります（例えば、太平洋標準時の `PST` と太平洋夏時間の `PDT`）。

時間値 *`offset`* は、GMT を基準とした時間または時間 :minutes 単位のタイムゾーンオフセットです。 例えば、`PDT` は `GMT -7` と同等です。

文字列形式の日付/時刻値のすべての要素が存在する必要があります。 日付/時刻の値が正しくフォーマットされていない場合、この値は無視され、代わりに [!DNL *`catalog`*.ini] ファイルの変更時刻が使用されます。

## 初期設定 {#section-ac465313c97943ed97d41ea852329177}

空の場合や定義されていない場合、サーバーはこの `*` カタログ `*.ini` ファイルのファイル変更時間を使用します。

## 関連項目 {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)、[attribute::UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8)、[attribute::CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
