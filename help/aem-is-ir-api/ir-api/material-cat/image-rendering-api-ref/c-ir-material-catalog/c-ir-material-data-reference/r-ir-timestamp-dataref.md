---
description: ファイル変更のタイムスタンプ。 このカタログレコードに添付されたイメージやデータファイルが最後に変更された日時を指定します。
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: ecc7617c-c390-4f82-905d-45b825d0176d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 1%

---

# TimeStamp{#timestamp}

ファイル変更のタイムスタンプ。 このカタログレコードに添付されたイメージやデータファイルが最後に変更された日時を指定します。

`attribute::UseLastModified`が設定されている場合、要求に関係するすべてのマテリアルとビネットの`catalog::TimeStamp`値と`vignette::TimeStamp`値の最新の値が、HTTP応答に最終変更ヘッダーとして返されます。

>[!NOTE]
>
>このカタログレコードに添付された画像またはデータファイルの実際のファイル時間は、この目的では使用されません。

`catalog::TimeStamp` は、カタログベースのキャッシュ検証にも使用されます( ` [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)`を参照)。

## プロパティ {#section-42f09e375e72492b87a3a486da7df808}

Java形式の日付/時間値。 1970年1月1日(UTC/GMT)の午前0時からのミリ秒の整数または次のいずれかの形式を持つ日付/時間文字列値を指定できます。

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*:  *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT  *[!DNL offset]*

* *[!DNL hh]* は0 ～ 23の範囲です。
* *[!DNL zzz]* は、「GMT」や「PST」などの3文字または4文字のタイムゾーンコードです。夏時間は、タイムゾーンコードで計算する必要があります（例えば、太平洋標準時の場合は「PST」、太平洋夏時間の場合は「PDT」）。
* *[!DNL offset]* は、GMTを基準とした、時間または時間：分単位のタイムゾーンオフセットです。例えば、「PDT」は「GMT -7」と同じです。

文字列形式の日付/時間値の要素はすべて存在する必要があります。 日付/時刻の値が正しい形式でない場合は無視され、代わりに&#x200B;*catalog*.iniファイルの変更時刻が使用されます。

## 初期設定 {#section-e2c126c9e7294662b23944ab8d14866b}

`attribute::TimeStamp` が空であるか、存在しない。

## 関連項目 {#section-876f1d1b50dc4501b605820015a29451}

[attribute::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) 、 [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)、 [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)、 [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
