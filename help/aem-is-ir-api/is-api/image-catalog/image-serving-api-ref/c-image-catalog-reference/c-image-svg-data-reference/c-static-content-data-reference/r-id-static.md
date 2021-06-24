---
description: ID
solution: Experience Manager
title: ID
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 818649dd-bcb7-4ff5-9308-6b5dc06f66e1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 5%

---

# ID{#id}

通常、SKU番号など、短く一意の識別子。SKUに複数の画像が含まれる場合や、ロケール固有のバリエーションが含まれる場合など、何らかのサフィックスが付く場合があります。 また、は、画像サービングを使用したWebサイトの再適合を容易にサポートするために、より複雑な文字列で、ファイルパスに似ている場合もあります。

>[!NOTE]
>
>画像カタログの読み込み時に、画像とSVGのテーブルが単一のテーブルに結合されます。 ID値は、両方のテーブルで一意である必要があります。 画像テーブルに同じID値を持つレコードが含まれている場合、SVGレコードは破棄されます。 静的コンテンツは別のテーブルで管理されます。静的コンテンツ項目と画像/SVG項目は、同じID値を持つ場合があります。

## プロパティ {#section-874a6853f67b4b229341ca76682884ae}

テキスト文字列。 必須。画像/SVGまたは静的コンテンツデータテーブルの識別子を記録します。 この画像カタログ/SVGカタログ内またはこの静的コンテンツカタログ内の各`catalog::Id`値は、一意である必要があり、「,」文字を含めることはできません。

## 初期設定 {#section-a26e7d83a5ee44b5918baef82ee48e14}

なし

## 関連項目 {#section-a258d818487d4ee6b7a99a65d18471a9}

[attribute::RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
