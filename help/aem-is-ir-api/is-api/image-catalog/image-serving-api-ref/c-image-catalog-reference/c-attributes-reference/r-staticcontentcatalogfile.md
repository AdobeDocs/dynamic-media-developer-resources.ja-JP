---
description: 静的コンテンツカタログデータファイルのパス このカタログの静的コンテンツデータを含むファイルを指定します。
seo-description: 静的コンテンツカタログデータファイルのパス このカタログの静的コンテンツデータを含むファイルを指定します。
seo-title: StaticContentCatalogFile
solution: Experience Manager
title: StaticContentCatalogFile
uuid: 82d2a68a-255a-4e65-a29f-7022e7f0f5ec
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 3%

---


# StaticContentCatalogFile{#staticcontentcatalogfile}

静的コンテンツカタログデータファイルのパス このカタログの静的コンテンツデータを含むファイルを指定します。

静的コンテンツカタログデータファイルは、指定された順序で読み込まれます。 同じ`static::Id`値が複数のレコード（同じカタログファイルまたは異なるカタログファイル）に存在する場合は、最後のインスタンスが使用されます。

## プロパティ {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

カンマで区切られた1つ以上のテキスト文字列値。 （オプション）各値は、絶対ファイルパスまたはカタログフォルダーを基準とした相対パスで指定する必要があります。

## 初期設定 {#section-702edfbc00c54fc29e412a3ff99fef2b}

空。この画像カタログに静的コンテンツデータが含まれていないことを示します。

## 関連項目 {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[カタログデータ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
