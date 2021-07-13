---
description: カタログレコード識別子
solution: Experience Manager
title: ID
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 37945115-c93d-4f59-b3d3-a2c4ee7fc990
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 7%

---

# ID {#id}

画像データファイル内のレコードをPlatform Serverが検索する際に使用するインデックスキー値。

通常、SKU番号など、SKUに複数の画像が含まれる場合に、画像のサフィックスが付く可能性がある、短く一意の画像識別子。 また、は、画像サービングを使用したWebサイトの再適合を容易にサポートするために、より複雑な文字列で、ファイルパスに似ている場合もあります。

## プロパティ {#id-properties}

テキスト文字列。 必須。プライマリデータテーブルの画像インデックスキー。 各catalog::Id値は、テーブル内で一意である必要があります。

## 初期設定 {#id-default}

なし

## 関連項目 {#id-seealso}

[attribute::RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)
