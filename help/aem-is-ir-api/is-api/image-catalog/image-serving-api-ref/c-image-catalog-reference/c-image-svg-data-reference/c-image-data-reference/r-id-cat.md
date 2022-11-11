---
description: カタログレコード識別子
solution: Experience Manager
title: ID
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 37945115-c93d-4f59-b3d3-a2c4ee7fc990
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 8%

---

# ID {#id}

イメージデータファイル内のレコードを検索する際に、 [!DNL Platform Server].

通常、SKU 番号など、SKU に複数の画像が含まれる場合に、何らかの画像サフィックスが付く、短く一意の画像識別子。 また、画像サービングを使用した Web サイトの再適合を容易にサポートするために、より複雑な文字列で、よりファイルパスに似ている場合もあります。

## プロパティ {#id-properties}

テキスト文字列。 必須。プライマリデータテーブルの画像インデックスキー。 各 catalog::Id 値は、テーブル内で一意である必要があります。

## 初期設定 {#id-default}

なし

## 関連項目 {#id-seealso}

[attribute::RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)
