---
description: 静的コンテンツカタログのデータファイルのパス。 このカタログの静的コンテンツ データを含むファイルを指定します。
solution: Experience Manager
title: StaticContentCatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ff6f0ad8-189f-4172-89cb-f138d2df8fe4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 2%

---

# StaticContentCatalogFile{#staticcontentcatalogfile}

静的コンテンツカタログのデータファイルのパス。 このカタログの静的コンテンツ データを含むファイルを指定します。

静的コンテンツカタログのデータファイルは、指定された順序で読み込まれます。 同じ `static::Id` 値が複数のレコード（同じカタログ ファイル内または異なるカタログ ファイル内）で発生した場合は、最後のインスタンスが優先されます。

## プロパティ {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

コンマで区切られた 1 つ以上のテキスト文字列値。 オプション。 各値は、絶対ファイルパスまたはカタログフォルダーを基準とした相対パスである必要があります。

## 初期設定 {#section-702edfbc00c54fc29e412a3ff99fef2b}

空。これは、この画像カタログに静的コンテンツデータが含まれていないことを示します。

## 関連項目 {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[カタログデータ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
