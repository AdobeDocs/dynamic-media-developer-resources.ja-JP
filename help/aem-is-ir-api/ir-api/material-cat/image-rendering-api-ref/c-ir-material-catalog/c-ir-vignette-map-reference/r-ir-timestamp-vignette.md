---
title: タイムスタンプ
description: 変更のタイムスタンプ。 このビネットが最後に変更された日時を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6a163727-9ac6-43ca-9afd-169ac6306124
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 1%

---

# タイムスタンプ{#timestamp}

変更のタイムスタンプ。 このビネットが最後に変更された日時を指定します。

`attribute::UseLastModified` が設定されている場合、ビネットの最新の `vignette::TimeStamp` と `catalog::TimeStamp` 値、およびリクエストに関連するすべてのマテリアルが、HTTP 応答で最終変更日のヘッダーとして返されます。

>[!NOTE]
>
>ビネットファイルの実際のファイル時間は、この目的には使用されません。

`catalog::TimeStamp` は、カタログベースのキャッシュ検証にも使用されます。 [attribute::CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md) を参照してください。

## プロパティ {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

Java™ 形式の日付/時刻値。 1970 年 1 月 1 日深夜 0 時からのミリ秒数の整数、1970 年 1 月 1 日の UTC/GMT、または日付/時刻の文字列値を次のいずれかの形式で指定します。

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]*GMT *[!DNL offset]*

* *[!DNL hh]* は 0～23 の範囲です。
* *[!DNL zzz]* は、「GMT」や「PST」など、3 文字または 4 文字のタイムゾーンコードです。 夏時間は、タイムゾーンコードで考慮する必要があります（例えば、太平洋標準時は「PST」、太平洋夏時間は「PDT」など）。
* *[!DNL offset]* は、GMT を基準とした時間または時間：分のタイムゾーンオフセットです。 例えば、「PDT」は「GMT -7」と同等です。

文字列形式の日付/時刻値のすべての要素が存在する必要があります。 日付/時刻の値が正しく設定されていない場合、この値は無視され、[!DNL *[!DNL catalog]*.ini] ファイルの変更時刻が代わりに使用されます。

## 初期設定 {#section-562c221d2e8b4a97ab5e9a3605f22140}

`attribute::TimeStamp` は、空または存在しないフィールドです。

## 関連項目 {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[attribute::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181)、[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)、[attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
