---
description: ID
solution: Experience Manager
title: ID
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 45a79636-3fa9-4f2a-98bb-a46c9b627dd4
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 5%

---


# ID{#id}

通常は、SKU番号など、短く一意な識別子です。SKUに複数の画像が含まれている場合や、ロケールによって異なる場合など、何らかのサフィックスが付く場合があります。 また、ファイルパスのように見える複雑な文字列にして、Webサイトを画像サービングで簡単に再適合できるようにすることもできます。

>[!NOTE]
>
>画像カタログが読み込まれると、画像とSVGテーブルが1つのテーブルに結合されます。 ID値は、両方のテーブルで一意である必要があります。 画像テーブルに同じID値を持つレコードが含まれている場合、SVGレコードは破棄されます。 静的コンテンツは別のテーブルで管理されます。したがって、静的コンテンツ項目と画像/SVG項目は同じId値を持つことがあります。

## プロパティ {#section-874a6853f67b4b229341ca76682884ae}

テキスト文字列。 必須。画像/SVGまたは静的コンテンツデータテーブルのレコード識別子。 この画像カタログ/SVGカタログ内またはこの静的コンテンツカタログ内の各`catalog::Id`値は、一意である必要があり、「,」文字を含めることはできません。

## 初期設定 {#section-a26e7d83a5ee44b5918baef82ee48e14}

なし

## 関連項目 {#section-a258d818487d4ee6b7a99a65d18471a9}

[attribute::RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
