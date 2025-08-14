---
title: タイムスタンプ
description: デフォルトの変更タイムスタンプ。 カタログのタイムスタンプとビネットのタイムスタンプのデフォルト値を提供します。 指定しない場合、サーバはこの catalog.ini ファイルの変更日時を使用します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b6d8fa6-0ad9-4f72-8d6d-1427e5d59df3
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 1%

---

# タイムスタンプ{#timestamp}

デフォルトの変更タイムスタンプ。 `catalog::TimeStamp` と `vignette::TimeStamp` のデフォルト値を指定します。 指定しない場合、サーバはこの catalog.ini ファイルの変更日時を使用します。

## プロパティ {#section-910e2562b41c47b78ee6216deeabbbd5}

Java™ 形式の日付/時刻値。 1970 年 1 月 1 日深夜 10 時からのミリ秒数を表す整数、または日付/時刻を表す文字列値を指定します。次のいずれかの形式を使用できます。

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

*[!DNL hh]* の範囲は 0 ～ 23 です。

*[!DNL zzz]* は、「GMT」や「PST」など、3 文字または 4 文字のタイムゾーンコードです。 夏時間は、タイムゾーンコードで考慮する必要があります（例えば、太平洋標準時は「PST」、太平洋夏時間は「PDT」など）。

*[!DNL offset]* は、GMT を基準とした時間または時 :minutes 単位のタイムゾーンオフセットです。 例えば、「PDT」は「GMT -7」と同等です。

文字列形式の日付/時刻値のすべての要素が存在する必要があります。 日付/時刻の値が正しく設定されていない場合、この値は無視され、[!DNL *[!DNL catalog]*.ini] ファイルの変更時刻が代わりに使用されます。

## 初期設定 {#section-65fb29a9ea2044df8cb9fe295eb14872}

空または定義されていない場合、サーバーはこの [!DNL *[!DNL catalog]*.ini] ファイルのファイル変更時刻を使用します。

## 関連項目 {#section-764188f9b1734ad1a6270f5fecd28532}

[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)、[vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)、[attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)、[attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)
