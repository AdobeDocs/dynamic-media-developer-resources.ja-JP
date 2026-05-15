---
title: TimeStamp
description: ファイル変更タイムスタンプ。 このカタログレコードに添付されている画像やデータファイルが最後に変更された日時を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ecc7617c-c390-4f82-905d-45b825d0176d
TQID: 'https://experienceleague.adobe.com/wC-1FowmCBdznH7ERWSYp-3Dx7bKC7fZPJXLnaWhFLU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 267
ht-degree: 1%

---

# TimeStamp{#timestamp}

ファイル変更タイムスタンプ。 このカタログレコードに添付されている画像やデータファイルが最後に変更された日時を指定します。

`attribute::UseLastModified`が設定されている場合、すべてのマテリアルの最新の`catalog::TimeStamp`値と`vignette::TimeStamp`値、およびリクエストに関係するビネットが、最終変更されたヘッダーとしてHTTP応答で返されます。

>[!NOTE]
>
>このカタログレコードに添付されている画像またはデータファイルの実際のファイル時間は、この目的では使用されません。

`catalog::TimeStamp`は、カタログベースのキャッシュ検証にも使用されます（[属性：:CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md)を参照）。

## プロパティ {#section-42f09e375e72492b87a3a486da7df808}

Java™形式の日時の値。 1970年1月1日の午前0時（UTC/GMT）からのミリ秒数の整数、または次のいずれかの形式の日付/時刻の文字列値を指定できます。

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

* *[!DNL hh]*&#x200B;は0 ～ 23の範囲です。
* *[!DNL zzz]*&#x200B;は、「GMT」や「PST」などの3文字または4文字のタイムゾーンコードです。 夏時間は、タイムゾーンコードで考慮する必要があります。 例えば、太平洋標準時の「PST」、太平洋夏時間の「PDT」などです。
* *[!DNL offset]*&#x200B;は、GMTに対する時間または時間:minutes単位のタイムゾーンオフセットです。 例えば、「PDT」は「GMT -7」と同等です。

文字列形式の日付/時刻値のすべての要素が存在する必要があります。 日付/時刻の値が正しくフォーマットされていない場合、その値は無視され、*カタログ*.ini ファイルの変更時間が代わりに使用されます。

## 初期設定 {#section-e2c126c9e7294662b23944ab8d14866b}

`attribute::TimeStamp`は空であるか、存在しないフィールドです。

## 関連項目 {#section-876f1d1b50dc4501b605820015a29451}

[属性：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181)、[属性：:UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)、[属性：:CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)、[ ビネット：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
