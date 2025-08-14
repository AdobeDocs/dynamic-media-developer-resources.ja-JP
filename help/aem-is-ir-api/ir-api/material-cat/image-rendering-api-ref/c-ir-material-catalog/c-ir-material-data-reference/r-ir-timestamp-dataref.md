---
title: タイムスタンプ
description: ファイル変更のタイムスタンプ。 このカタログ レコードにアタッチされたイメージやデータ ファイルが最後に修正された日時を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ecc7617c-c390-4f82-905d-45b825d0176d
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 1%

---

# タイムスタンプ{#timestamp}

ファイル変更のタイムスタンプ。 このカタログ レコードにアタッチされたイメージやデータ ファイルが最後に修正された日時を指定します。

`attribute::UseLastModified` が設定されている場合、リクエストに関係するすべてのマテリアルとビネットの最新の `catalog::TimeStamp` と `vignette::TimeStamp` の値が、HTTP 応答で最終変更日のヘッダーとして返されます。

>[!NOTE]
>
>このカタログレコードに添付された画像またはデータファイルの実際のファイル時間は、この目的には使用されません。

`catalog::TimeStamp` は、カタログベースのキャッシュ検証にも使用されます（[attribute::CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md) を参照）。

## プロパティ {#section-42f09e375e72492b87a3a486da7df808}

Java™ 形式の日付/時刻値。 1970 年 1 月 1 日深夜 0 時からのミリ秒数の整数、1970 年 1 月 1 日の UTC/GMT、または日付/時刻の文字列値を次のいずれかの形式で指定します。

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

* *[!DNL hh]* は 0～23 の範囲です。
* *[!DNL zzz]* は、「GMT」や「PST」など、3 文字または 4 文字のタイムゾーンコードです。 夏時間は、タイムゾーンコードで考慮する必要があります。 例えば、太平洋標準時は「PST」、太平洋夏時間は「PDT」です。
* *[!DNL offset]* は、GMT を基準とした時間または時 :minutes 単位のタイムゾーンオフセットです。 例えば、「PDT」は「GMT -7」と同等です。

文字列形式の日付/時刻値のすべての要素が存在する必要があります。 日付/時刻の値が正しくフォーマットされていない場合、この値は無視され、代わりに *catalog*.ini ファイルの変更時刻が使用されます。

## 初期設定 {#section-e2c126c9e7294662b23944ab8d14866b}

`attribute::TimeStamp` は、空または存在しないフィールドです。

## 関連項目 {#section-876f1d1b50dc4501b605820015a29451}

[attribute::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181)、[attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)、[attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)、[vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
