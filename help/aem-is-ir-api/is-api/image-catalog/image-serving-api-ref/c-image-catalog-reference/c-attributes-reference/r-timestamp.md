---
title: TimeStamp
description: デフォルトの画像修正タイムスタンプ。 カタログのTimeStampのデフォルト値を提供します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e137f795-e0f7-4b72-b7e8-188e254bbb45
TQID: 'https://experienceleague.adobe.com/Wyj0OJrb0URsXaymXmx1aB82Qyxun1HatBUqBS4F6cE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 209
ht-degree: 1%

---

# TimeStamp{#timestamp}

デフォルトの画像修正タイムスタンプ。 catalog::TimeStampのデフォルト値を指定します。

指定しない場合、サーバーはこの&#x200B;[!DNL *`catalog`*.ini] ファイルの変更日時を使用します。

## プロパティ {#section-647066e62ce44a84b627fdd0b2f7cfec}

日付/時刻の値。 1970年1月1日の午前0時（UTC/GMT）からのミリ秒数の整数、または次のいずれかの形式の日付/時刻の文字列値を指定できます。

日時の値&#x200B;*`mm`*/*`dd`*/*`yyyy`* *`hh`*: *`mm`*: *`ss zzz`*

日付/時刻の値&#x200B;*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT *`offset`*

時間の値&#x200B;*`hh`*&#x200B;は0 ～ 23の範囲です。

時間の値&#x200B;*`zzz`*&#x200B;は、`GMT`や`PST`などの3文字または4文字のタイムゾーンコードです。 夏時間は、タイムゾーンコードで考慮する必要があります（例えば、太平洋標準時は`PST`、太平洋夏時間は`PDT`）。

時間値&#x200B;*`offset`*&#x200B;は、GMTに対する時間または時間:minutes単位のタイムゾーンオフセットです。 例えば、`PDT`は`GMT -7`と同等です。

文字列形式の日付/時刻値のすべての要素が存在する必要があります。 日付/時刻の値が正しくフォーマットされていない場合、その値は無視され、[!DNL *`catalog`*.ini] ファイルの変更時間が代わりに使用されます。

## 初期設定 {#section-ac465313c97943ed97d41ea852329177}

空または定義されていない場合、サーバーはこの`*` カタログ `*.ini` ファイルのファイル変更時間を使用します。

## 関連項目 {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[&#x200B; カタログ：:TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)、[属性：:UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8)、[属性：:CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
