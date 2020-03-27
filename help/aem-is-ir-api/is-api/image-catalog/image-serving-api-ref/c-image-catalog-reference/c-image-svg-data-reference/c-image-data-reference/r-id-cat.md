---
description: カタログレコード識別子
solution: Experience Manager
title: ID
topic: Scene7 Image Serving - Image Rendering API
uuid: 9803d754-1f94-4e5d-9a40-3936676c0035
translation-type: tm+mt
source-git-commit: 7d3902803d42f5d479dd04ac9470a4088809f3d6

---


# ID {#id}

画像データファイル内のレコードがプラットフォームサーバーによって検索されるインデックスキー値。

通常、SKU番号など、短く一意の画像識別子。SKUに複数の画像が含まれる場合は、何らかの画像サフィックスが付くことがあります。 また、ファイルパスに似た複雑な文字列を使用して、画像サービングでWebサイトを簡単に再調整できるようにすることもできます。

## プロパティ {#id-properties}

テキスト文字列。 必須。画像データテーブルのプライマリインデックスキー。 各catalog::Id値は、テーブル内で一意である必要があります。

## 初期設定 {#id-default}

なし

## 関連項目 {#id-seealso}

[attribute::RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)