---
description: ファイル変更のタイムスタンプ。 このカタログレコードに添付されているイメージやデータファイルが最後に変更された日時を指定します。
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ecc7617c-c390-4f82-905d-45b825d0176d
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 1%

---

# TimeStamp{#timestamp}

ファイル変更のタイムスタンプ。 このカタログレコードに添付されているイメージやデータファイルが最後に変更された日時を指定します。

If `attribute::UseLastModified` が設定されている場合、 `catalog::TimeStamp` および `vignette::TimeStamp` リクエストに関連するすべてのマテリアルとビネットの値は、HTTP 応答で最終変更ヘッダーとして返されます。

>[!NOTE]
>
>このカタログレコードに添付されている画像やデータファイルの実際のファイル時間は、この目的では使用されません。

`catalog::TimeStamp` は、カタログベースのキャッシュ検証にも使用されます ( [attribute::CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md)) をクリックします。

## プロパティ {#section-42f09e375e72492b87a3a486da7df808}

Java 形式の日時値。 1970 年 1 月 1 日 (UTC/GMT) 午前 0 時からのミリ秒の整数か、次のいずれかの形式を持つ日付/時間文字列値を指定できます。

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

* *[!DNL hh]* は 0 ～ 23 の範囲です。
* *[!DNL zzz]* は、「GMT」や「PST」などの 3 文字または 4 文字のタイムゾーンコードです。 夏時間は、タイムゾーンコードで考慮する必要があります（例えば、太平洋標準時の場合は「PST」、太平洋夏時間の場合は「PDT」）。
* *[!DNL offset]* は、GMT を基準とした、時間または時間：分単位のタイムゾーンオフセットです。 例えば、「PDT」は「GMT -7」と同じです。

文字列形式の日付/時刻値の要素はすべて存在する必要があります。 日付/時刻値の形式が正しくない場合、その値は無視され、変更時刻は *カタログ*&#x200B;代わりに、 .ini ファイルが使用されます。

## 初期設定 {#section-e2c126c9e7294662b23944ab8d14866b}

`attribute::TimeStamp` が空の場合や存在しない場合。

## 関連項目 {#section-876f1d1b50dc4501b605820015a29451}

[attribute::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d), [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4), [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
