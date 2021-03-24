---
description: カタログレコード識別子
solution: Experience Manager
title: ID
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 7%

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