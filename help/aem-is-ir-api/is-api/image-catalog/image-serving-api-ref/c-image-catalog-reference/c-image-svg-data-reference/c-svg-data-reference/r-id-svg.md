---
title: ID
description: 通常は、SKU 番号などの短い一意の ID で、SKU に複数の画像がある場合やロケール固有のバリエーションがある場合など、何らかのサフィックスが付いている場合があります。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d7b37180-cc93-41cd-bf14-5c262b046fbc
source-git-commit: c1a4dad7888d31e0b78f0fc5091700ad8104e685
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 3%

---

# ID{#id}

通常は、SKU 番号などの短い一意の ID で、SKU に複数の画像がある場合やロケール固有のバリエーションがある場合など、何らかのサフィックスが付いている場合があります。 また、は、画像サービングで web サイトを簡単に調整できるように、ファイルパスのように見えるより複雑な文字列になる場合があります。

>[!NOTE]
>
>画像カタログが読み込まれると、画像テーブルとSVGテーブルが 1 つのテーブルに結合されます。 Id 値は両方のテーブルで一意である必要があります。 画像テーブルに同じ ID 値を持つレコードが含まれている場合、SVGレコードは破棄されます。 静的コンテンツは、別個のテーブルで管理されます。したがって、静的コンテンツ項目と画像/SVG項目は、同じ ID 値を持つ場合があります。

## プロパティ {#section-874a6853f67b4b229341ca76682884ae}

テキスト文字列 必須。 画像/SVGまたは静的コンテンツデータテーブルのレコード識別子。 この画像カタログ/SVGカタログ内、またはこの静的コンテンツカタログ内の各 `catalog::Id` 値は、一意である必要があり、「,」を含めることはできません。

## 初期設定 {#section-a26e7d83a5ee44b5918baef82ee48e14}

なし

## 関連項目 {#section-a258d818487d4ee6b7a99a65d18471a9}

[attribute::RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
