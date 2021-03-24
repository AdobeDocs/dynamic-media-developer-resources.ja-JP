---
description: 静的コンテンツカタログデータファイルのパス このカタログの静的コンテンツデータを含むファイルを指定します。
solution: Experience Manager
title: StaticContentCatalogFile
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 4%

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
