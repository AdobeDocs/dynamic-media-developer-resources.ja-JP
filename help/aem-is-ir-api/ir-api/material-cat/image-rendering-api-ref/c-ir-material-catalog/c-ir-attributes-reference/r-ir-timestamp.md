---
description: デフォルトの変更タイムスタンプ。 カタログのTimeStampとビネットのTimeStampの初期設定値を指定します。 指定しなかった場合、サーバはこのcatalog.iniファイルの変更日時を使用します。
seo-description: デフォルトの変更タイムスタンプ。 カタログのTimeStampとビネットのTimeStampの初期設定値を指定します。 指定しなかった場合、サーバはこのcatalog.iniファイルの変更日時を使用します。
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Scene7 Image Serving - Image Rendering API
uuid: 10ceb600-1ed9-46a1-ae07-889d601ac0f4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 1%

---


# TimeStamp{#timestamp}

デフォルトの変更タイムスタンプ。 catalog::TimeStampとvignet::TimeStampの初期設定値を指定します。 指定しなかった場合、サーバはこのcatalog.iniファイルの変更日時を使用します。

## プロパティ {#section-910e2562b41c47b78ee6216deeabbbd5}

Java形式の日付/時間値。 1970年1月1日(UTC/GMT)、1970年1月1日からのミリ秒の整数値、または次のいずれかの形式の日付/時間文字列値を指定できます。

* *[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*:  *[!DNL ss]* *[!DNL zzz]*

* *[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT  *[!DNL offset]*

*[!DNL hh]* は0 ～ 23の範囲にあります。

*[!DNL zzz]* は、「GMT」や「PST」などの3文字または4文字のタイムゾーンコードです。夏時間は、タイムゾーンコードで考慮する必要があります（例えば、太平洋標準時の場合は「PST」、太平洋夏時間の場合は「PDT」）。

*[!DNL offset]* は、GMTを基準とした、時間または時間：分単位のタイムゾーンオフセットです。例えば、「PDT」は「GMT -7」と同じです。

日付/時間形式の文字列値の要素はすべて存在する必要があります。 日付/時刻値の形式が正しくない場合は無視され、[!DNL *[!DNL catalog]*.ini]ファイルの変更時刻が代わりに使用されます。

## 初期設定 {#section-65fb29a9ea2044df8cb9fe295eb14872}

空の場合、または定義されていない場合、サーバーはこの[!DNL *[!DNL catalog]*.ini]ファイルのファイル変更時刻を使用します。

## 関連項目 {#section-764188f9b1734ad1a6270f5fecd28532}

[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) ,  [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1),  [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d),  [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)
