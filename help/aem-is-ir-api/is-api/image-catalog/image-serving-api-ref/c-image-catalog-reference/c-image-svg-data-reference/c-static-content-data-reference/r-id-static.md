---
title: ID
description: 通常は、SKU番号などの短い一意の識別子（SKUに複数の画像がある場合や、ロケール固有のバリエーションがある場合など）をサフィックスの一部として使用します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 818649dd-bcb7-4ff5-9308-6b5dc06f66e1
TQID: 'https://experienceleague.adobe.com/xPBbjaHO58J-4HFnChD1ybEVoE2AbRZuFVA8nbquEvg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 3%

---

# ID{#id}

通常は、SKU番号などの短い一意の識別子。SKUに複数の画像がある場合や、ロケール固有のバリエーションがある場合など、何らかの接尾辞が付いている可能性があります。 また、画像サービングを使用してweb サイトを簡単に再構成できるように、ファイルパスのように見える、より複雑な文字列を指定することもできます。

>[!NOTE]
>
>画像カタログが読み込まれると、画像テーブルとSVG テーブルが1つのテーブルに結合されます。 Id値は、両方のテーブルで一意である必要があります。 画像テーブルに同じID値を持つレコードが含まれている場合、SVG レコードは破棄されます。 静的コンテンツは別のテーブルで管理されます。静的コンテンツ項目と画像/SVG項目のID値は同じである場合があります。

## プロパティ {#section-874a6853f67b4b229341ca76682884ae}

テキスト文字列。 必須。 image/SVGまたは静的コンテンツデータテーブルのレコード識別子。 この画像カタログ/SVG カタログ内または静的コンテンツカタログ内の各`catalog::Id`値は一意である必要があり、「,」文字を含めることはできません。

## 初期設定 {#section-a26e7d83a5ee44b5918baef82ee48e14}

なし

## 関連項目 {#section-a258d818487d4ee6b7a99a65d18471a9}

[属性：:RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
