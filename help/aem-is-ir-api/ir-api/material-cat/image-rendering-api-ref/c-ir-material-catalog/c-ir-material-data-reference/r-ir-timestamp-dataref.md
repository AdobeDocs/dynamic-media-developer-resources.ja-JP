---
description: ファイル変更のタイムスタンプ。 このカタログレコードに添付された画像ファイルやデータファイルが最後に変更された日時を指定します。
seo-description: ファイル変更のタイムスタンプ。 このカタログレコードに添付された画像ファイルやデータファイルが最後に変更された日時を指定します。
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Scene7 Image Serving - Image Rendering API
uuid: 77ce8bee-7b55-4ff8-8dfb-ebd3ce9c7a8a
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 1%

---


# TimeStamp{#timestamp}

ファイル変更のタイムスタンプ。 このカタログレコードに添付された画像ファイルやデータファイルが最後に変更された日時を指定します。

を設定 `attribute::UseLastModified` すると、要求に関連するすべてのマテリアル `catalog::TimeStamp``vignette::TimeStamp` とビネットの最新の値と値が、HTTP応答で最後に変更されたヘッダーとして返されます。

>[!NOTE]
>
>このカタログレコードに添付された画像またはデータファイルの実際のファイル時間は、この目的では使用されません。

`catalog::TimeStamp` は、カタログベースのキャッシュ検証にも使用されます(を参照 ` [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)`)。

## プロパティ {#section-42f09e375e72492b87a3a486da7df808}

Java形式の日付/時間値。 1970年1月1日(UTC/GMT)、1970年1月1日からのミリ秒の整数値、または次のいずれかの形式の日付/時間文字列値を指定できます。

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]**[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

* *[!DNL hh]* は0 ～ 23の範囲にあります。
* *[!DNL zzz]* は、「GMT」や「PST」などの3文字または4文字のタイムゾーンコードです。 夏時間は、タイムゾーンコードで考慮する必要があります（例えば、太平洋標準時の場合は「PST」、太平洋夏時間の場合は「PDT」）。
* *[!DNL offset]* は、GMTを基準とした、時間または時間：分単位のタイムゾーンオフセットです。 例えば、「PDT」は「GMT -7」と同じです。

日付/時間形式の文字列値の要素はすべて存在する必要があります。 日付/時刻値の形式が正しくない場合は無視され、 *catalog*.iniファイルの変更時刻が代わりに使用されます。

## 初期設定 {#section-e2c126c9e7294662b23944ab8d14866b}

`attribute::TimeStamp` が空か存在しないフィールドです。

## 関連項目 {#section-876f1d1b50dc4501b605820015a29451}

[attribute::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d), [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4), [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
