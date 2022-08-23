---
title: TimeStamp
description: デフォルトの変更タイムスタンプ。 カタログの TimeStamp とビネットの TimeStamp のデフォルト値を指定します。 指定しなかった場合、サーバはこの catalog.ini ファイルの変更日時を使用します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b6d8fa6-0ad9-4f72-8d6d-1427e5d59df3
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# TimeStamp{#timestamp}

デフォルトの変更タイムスタンプ。 のデフォルト値を指定します。 `catalog::TimeStamp` および `vignette::TimeStamp`. 指定しなかった場合、サーバはこの catalog.ini ファイルの変更日時を使用します。

## プロパティ {#section-910e2562b41c47b78ee6216deeabbbd5}

Java™形式の日付/時間値。 1970 年 1 月 1 日 (UTC/GMT) 午前 0 時からのミリ秒の整数か、次のいずれかの形式を持つ日付/時間文字列値を指定できます。

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

*[!DNL hh]* は 0 ～ 23 の範囲です。

*[!DNL zzz]* は、「GMT」や「PST」などの 3 文字または 4 文字のタイムゾーンコードです。 夏時間は、タイムゾーンコードで考慮する必要があります（例えば、太平洋標準時の場合は「PST」、太平洋夏時間の場合は「PDT」）。

*[!DNL offset]* は、GMT を基準とした、時間または時間：分単位のタイムゾーンオフセットです。 例えば、「PDT」は「GMT -7」と同じです。

文字列形式の日付/時刻値の要素はすべて存在する必要があります。 日付/時刻の値が正しい形式でない場合、その値は無視され、変更時刻は [!DNL *[!DNL catalog]*&#x200B;代わりに、 .ini] ファイルが使用されます。

## 初期設定 {#section-65fb29a9ea2044df8cb9fe295eb14872}

空の場合または定義されていない場合、サーバーはこの [!DNL *[!DNL catalog]*.ini] ファイル

## 関連項目 {#section-764188f9b1734ad1a6270f5fecd28532}

[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1), [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d), [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)
