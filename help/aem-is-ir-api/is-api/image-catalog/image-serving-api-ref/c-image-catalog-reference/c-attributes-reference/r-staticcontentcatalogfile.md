---
description: 静的コンテンツカタログデータファイルのパス。 このカタログの静的コンテンツデータを含むファイルを指定します。
solution: Experience Manager
title: StaticContentCatalogFile
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: ff6f0ad8-189f-4172-89cb-f138d2df8fe4
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 4%

---

# StaticContentCatalogFile{#staticcontentcatalogfile}

静的コンテンツカタログデータファイルのパス。 このカタログの静的コンテンツデータを含むファイルを指定します。

静的コンテンツカタログデータファイルは、指定された順序で読み込まれます。 複数のレコード（同じカタログファイルまたは異なるカタログファイル）に同じ`static::Id`値が含まれる場合は、最後のインスタンスが優先されます。

## プロパティ {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

コンマ区切りの1つ以上のテキスト文字列値。 （オプション）各値は、絶対ファイルパスまたはカタログフォルダーを基準とした相対パスである必要があります。

## 初期設定 {#section-702edfbc00c54fc29e412a3ff99fef2b}

空の場合は、この画像カタログに静的コンテンツデータが含まれていないことを示します。

## 関連項目 {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[カタログデータ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
