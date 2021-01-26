---
description: カタログレコード識別子
solution: Experience Manager
title: ID
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9803d754-1f94-4e5d-9a40-3936676c0035
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 8%

---


# ID {#id}

画像データファイル内のレコードがプラットフォームサーバーによって検索されるインデックスキー値。

通常、SKU番号など、SKUに複数の画像が含まれる場合、画像のサフィックスが何らかの場合がある、短く一意な画像識別子。 また、より複雑な文字列で、ファイルパスのように見える場合もあります。これにより、画像サービングを使用したWebサイトの遡及的な調整が容易にサポートされます。

## プロパティ {#id-properties}

テキスト文字列。 必須。画像データテーブルのプライマリインデックスキー。 各catalog::Idの値は、テーブル内で一意である必要があります。

## 初期設定 {#id-default}

なし

## 関連項目 {#id-seealso}

[attribute::RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)