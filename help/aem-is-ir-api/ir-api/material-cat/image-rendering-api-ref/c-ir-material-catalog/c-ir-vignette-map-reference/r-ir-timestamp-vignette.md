---
title: TimeStamp
description: 修正タイムスタンプ。 このビネットが最後に変更された日時を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6a163727-9ac6-43ca-9afd-169ac6306124
TQID: 'https://experienceleague.adobe.com/lVoM4P1NUj-ugSgiBM5l-9L9wtTuGiZCKDjTnEGQa1A'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 237
ht-degree: 1%

---

# TimeStamp{#timestamp}

修正タイムスタンプ。 このビネットが最後に変更された日時を指定します。

`attribute::UseLastModified`が設定されている場合、ビネットの最新の`vignette::TimeStamp`と`catalog::TimeStamp`値、およびリクエストに関連するすべてのマテリアルが、最終変更されたヘッダーとしてHTTP応答で返されます。

>[!NOTE]
>
>ビネットファイルの実際のファイル時間は、この目的では使用されません。

`catalog::TimeStamp`は、カタログベースのキャッシュ検証にも使用されます。 [attribute::CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md)を参照してください。

## プロパティ {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

Java™形式の日時の値。 1970年1月1日の午前0時（UTC/GMT）からのミリ秒数の整数、または次のいずれかの形式の日付/時刻の文字列値を指定できます。

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]*&#x200B;GMT *[!DNL offset]*

* *[!DNL hh]*&#x200B;は0 ～ 23の範囲です。
* *[!DNL zzz]*&#x200B;は、「GMT」や「PST」などの3文字または4文字のタイムゾーンコードです。 夏時間は、タイムゾーンコードで考慮する必要があります（例えば、太平洋標準時の「PST」、太平洋夏時間の「PDT」など）。
* *[!DNL offset]*&#x200B;は、GMTに対する時間または時間:minutes単位のタイムゾーンオフセットです。 例えば、「PDT」は「GMT -7」と同等です。

文字列形式の日付/時刻値のすべての要素が存在する必要があります。 日付/時刻の値が正しくフォーマットされていない場合、その値は無視され、[!DNL *[!DNL catalog]*.ini] ファイルの変更時間が代わりに使用されます。

## 初期設定 {#section-562c221d2e8b4a97ab5e9a3605f22140}

`attribute::TimeStamp`は空であるか、存在しないフィールドです。

## 関連項目 {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[属性：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181)、[&#x200B; カタログ：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)、[属性：:UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
