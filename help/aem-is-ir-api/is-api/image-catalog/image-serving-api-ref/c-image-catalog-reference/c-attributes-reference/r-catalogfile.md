---
description: 画像データファイルのパス このカタログの画像データを含むファイルを指定します。
seo-description: 画像データファイルのパス このカタログの画像データを含むファイルを指定します。
seo-title: CatalogFile
solution: Experience Manager
title: CatalogFile
topic: Scene7 Image Serving - Image Rendering API
uuid: 3599c8d3-dc4b-434e-8b11-775ea6f155ee
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 4%

---


# CatalogFile{#catalogfile}

画像データファイルのパス このカタログの画像データを含むファイルを指定します。

画像データファイルは、指定された順序で読み込まれます。 同じ`catalog::Id`値が複数のレコード（同じカタログファイルまたは異なるカタログファイル）に存在する場合は、最後のインスタンスが使用されます。

## プロパティ {#section-6da55f145ecd4e31a5de52637a436983}

カンマで区切られた1つ以上のテキスト文字列値。 （オプション）各値は、絶対ファイルパスまたはカタログフォルダーを基準とした相対パスで指定する必要があります。

## 初期設定 {#section-80f91cd7a6b2479ebb310319e9c74da7}

空。この画像カタログに画像データが含まれていないことを示します。

## 関連項目 {#section-910b67c5041d44d99a105ad43ff63a37}

[カタログデータフィールド](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
