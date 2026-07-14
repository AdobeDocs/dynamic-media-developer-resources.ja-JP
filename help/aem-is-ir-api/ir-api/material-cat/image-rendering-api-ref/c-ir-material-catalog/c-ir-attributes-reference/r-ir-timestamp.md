---
title: TimeStamp
description: デフォルトの修正タイムスタンプ。 カタログ TimeStampおよび周辺光量補正TimeStampのデフォルト値を提供します。 指定しない場合、サーバーはこのcatalog.ini ファイルの変更日時を使用します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b6d8fa6-0ad9-4f72-8d6d-1427e5d59df3
TQID: 'https://experienceleague.adobe.com/p3g5NQf25sagtaAYjdd4Vd8J6kZBAoLM8tSY42NPuOI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 232
ht-degree: 7%

---

# TimeStamp{#timestamp}

デフォルトの修正タイムスタンプ。 `catalog::TimeStamp`および`vignette::TimeStamp`の既定値を指定します。 指定しない場合、サーバーはこのcatalog.ini ファイルの変更日時を使用します。

## プロパティ {#section-910e2562b41c47b78ee6216deeabbbd5}

Java™形式の日時の値。 1970年1月1日の午前0時（UTC/GMT）からのミリ秒数の整数、または次のいずれかの形式の日付/時刻の文字列値を指定できます。

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

*[!DNL hh]*&#x200B;は0 ～ 23の範囲です。

*[!DNL zzz]*&#x200B;は、「GMT」や「PST」などの3文字または4文字のタイムゾーンコードです。 夏時間は、タイムゾーンコードで考慮する必要があります（例えば、太平洋標準時の「PST」、太平洋夏時間の「PDT」など）。

*[!DNL offset]*&#x200B;は、GMTに対する時間または時間:minutes単位のタイムゾーンオフセットです。 例えば、「PDT」は「GMT -7」と同等です。

文字列形式の日付/時刻値のすべての要素が存在する必要があります。 日付/時刻の値が正しくフォーマットされていない場合、その値は無視され、[!DNL *[!DNL catalog]*.ini] ファイルの変更時間が代わりに使用されます。

## 初期設定 {#section-65fb29a9ea2044df8cb9fe295eb14872}

空または定義されていない場合、サーバーはこの[!DNL *[!DNL catalog]*.ini] ファイルのファイル変更時間を使用します。

## 関連項目 {#section-764188f9b1734ad1a6270f5fecd28532}

[&#x200B; カタログ：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)、[&#x200B; ビネット：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)、[属性：:UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)、[属性：:CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)

