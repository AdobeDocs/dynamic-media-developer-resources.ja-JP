---
description: 画像データファイルのパス。 このカタログの画像データを含むファイルを指定します。
solution: Experience Manager
title: CatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 240a3884-68dd-474c-83a6-d79fc5b6c300
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 2%

---

# CatalogFile{#catalogfile}

画像データファイルのパス。 このカタログの画像データを含むファイルを指定します。

画像データファイルは、指定された順序で読み込まれます。 同じ `catalog::Id` 値が複数のレコード（同じカタログ ファイル内または異なるカタログ ファイル内）で発生した場合は、最後のインスタンスが優先されます。

## プロパティ {#section-6da55f145ecd4e31a5de52637a436983}

コンマで区切られた 1 つ以上のテキスト文字列値。 オプション。 各値は、絶対ファイルパスまたはカタログフォルダーを基準とした相対パスである必要があります。

## 初期設定 {#section-80f91cd7a6b2479ebb310319e9c74da7}

空。これは、この画像カタログに画像データが含まれていないことを示します。

## 関連項目 {#section-910b67c5041d44d99a105ad43ff63a37}

[カタログデータフィールド](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
