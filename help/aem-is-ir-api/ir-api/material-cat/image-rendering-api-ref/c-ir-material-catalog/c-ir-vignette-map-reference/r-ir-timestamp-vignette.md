---
description: 変更のタイムスタンプ。 このビネットが最後に変更された日時を指定します。
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6a163727-9ac6-43ca-9afd-169ac6306124
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 1%

---

# TimeStamp{#timestamp}

変更のタイムスタンプ。 このビネットが最後に変更された日時を指定します。

If `attribute::UseLastModified` が設定されている場合、最新 `vignette::TimeStamp` および `catalog::TimeStamp`ビネットの値と、要求に関係するすべてのマテリアルが、最終変更ヘッダーとして HTTP 応答に返されます。

>[!NOTE]
>
>ビネットファイルの実際のファイル時間は、この目的には使用されません。

`catalog::TimeStamp` は、カタログベースのキャッシュ検証にも使用されます ( ` [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)`) をクリックします。

## プロパティ {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

Java 形式の日時値。 1970 年 1 月 1 日 (UTC/GMT) 午前 0 時からのミリ秒の整数か、次のいずれかの形式を持つ日付/時間文字列値を指定できます。

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*:*[!DNL ss]*GMT *[!DNL offset]*

* *[!DNL hh]* は 0 ～ 23 の範囲です。
* *[!DNL zzz]* は、「GMT」や「PST」などの 3 文字または 4 文字のタイムゾーンコードです。 夏時間は、タイムゾーンコードで考慮する必要があります（例えば、太平洋標準時の場合は「PST」、太平洋夏時間の場合は「PDT」）。
* *[!DNL offset]* は、GMT を基準とした、時間または時間：分単位のタイムゾーンオフセットです。 例えば、「PDT」は「GMT -7」と同じです。

文字列形式の日付/時刻値の要素はすべて存在する必要があります。 日付/時刻の値が正しい形式でない場合、その値は無視され、[!DNL *[!DNL catalog]*&#x200B;代わりに、 .ini] ファイルが使用されます。

## 初期設定 {#section-562c221d2e8b4a97ab5e9a3605f22140}

`attribute::TimeStamp` が空の場合や存在しない場合。

## 関連項目 {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[attribute::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319), [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
