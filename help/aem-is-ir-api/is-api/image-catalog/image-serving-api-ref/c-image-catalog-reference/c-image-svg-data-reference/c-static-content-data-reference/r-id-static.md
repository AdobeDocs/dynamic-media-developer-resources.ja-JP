---
description: 'null'
seo-description: 'null'
seo-title: ID
solution: Experience Manager
title: ID
topic: Scene7 Image Serving - Image Rendering API
uuid: 45a79636-3fa9-4f2a-98bb-a46c9b627dd4
translation-type: tm+mt
source-git-commit: 7721cccf3f779f258adcdcf886f7e01111e92be0

---


# ID{#id}

通常は、SKU番号など、短く一意の識別子です。SKUに複数の画像が含まれている場合や、ロケールに固有のバリエーションが含まれている場合など、何らかのサフィックスを持つ場合があります。 また、ファイルパスに似た複雑な文字列を使用して、Webサイトを画像サービングで簡単に再調整できるようにすることもできます。

>[!NOTE]
>
>画像カタログが読み込まれると、画像とSVGテーブルが単一のテーブルに結合されます。 ID値は、両方のテーブルで一意である必要があります。 画像テーブルに同じID値を持つレコードが含まれている場合、SVGレコードは破棄されます。 静的コンテンツは別の表で管理されます。静的コンテンツ項目と画像/SVG項目は同じID値を持つ場合があります。

## プロパティ {#section-874a6853f67b4b229341ca76682884ae}

テキスト文字列。 必須。画像/SVGまたは静的コンテンツデータテーブルの識別子を記録します。 この画 `catalog::Id` 像カタログ/SVGカタログまたはこの静的コンテンツカタログ内の各値は、一意で、「,」文字を含めないでください。

## 初期設定 {#section-a26e7d83a5ee44b5918baef82ee48e14}

なし

## 関連項目 {#section-a258d818487d4ee6b7a99a65d18471a9}

[attribute::RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
