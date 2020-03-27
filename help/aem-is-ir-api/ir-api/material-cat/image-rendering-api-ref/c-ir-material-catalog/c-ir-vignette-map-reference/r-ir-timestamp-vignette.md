---
description: 変更のタイムスタンプ。 このビネットが最後に修正された日時を指定します。
seo-description: 変更のタイムスタンプ。 このビネットが最後に修正された日時を指定します。
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Scene7 Image Serving - Image Rendering API
uuid: d2649e86-8a6f-4f63-ab6a-8b2d8c03f8c0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# TimeStamp{#timestamp}

変更のタイムスタンプ。 このビネットが最後に修正された日時を指定します。

を設定 `attribute::UseLastModified` すると、ビネットの `vignette::TimeStamp` 最新 `catalog::TimeStamp`と値、および要求に関連するすべてのマテリアルが、最終変更時のヘッダーとしてHTTP応答に返されます。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>ビネットファイルの実際のファイル時間は、この目的では使用されません。

`catalog::TimeStamp` は、カタログベースのキャッシュ検証にも使用されます(を参照 ` [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)`)。

## プロパティ {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

Java形式の日付/時間値。 1970年1月1日0時(UTC/GMT)からのミリ秒の整数または日時文字列値で、次のいずれかの形式を使用できます。

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]**[!DNL hh]*: *[!DNL mm]*:*[!DNL ss]*GMT *[!DNL offset]*

* *[!DNL hh]* は0 ～ 23の範囲です。
* *[!DNL zzz]* は、「GMT」や「PST」などの3文字または4文字のタイムゾーンコードです。 夏時間は、タイムゾーンコードで計上する必要があります（例えば、太平洋標準時の場合は「PST」、太平洋夏時間の場合は「PDT」）。
* *[!DNL offset]* は、GMTを基準とした時間または時間：分単位のタイムゾーンのオフセットです。 例えば、「PDT」は「GMT -7」と同じです。

日付/時間の形式を設定した文字列の要素はすべて存在する必要があります。 日付/時刻値の形式が正しくない場合は無視され、[!DNL *[!DNL catalog]*.ini]ファイルの変更時刻が代わりに使用されます。

## 初期設定 {#section-562c221d2e8b4a97ab5e9a3605f22140}

`attribute::TimeStamp` が空か、存在しない場合。

## 関連項目 {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[attribute::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) 、 [catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)、 [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
