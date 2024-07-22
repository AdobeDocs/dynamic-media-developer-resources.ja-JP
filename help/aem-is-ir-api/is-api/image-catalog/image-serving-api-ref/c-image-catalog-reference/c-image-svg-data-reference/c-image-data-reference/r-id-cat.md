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
ht-degree: 6%

---

# ID {#id}

イメージ データ ファイル内のレコードを [!DNL Platform Server] で検索するためのインデックス キー値です。

通常は、SKU に複数の画像がある場合は、SKU 番号などの短い一意の画像識別子に何らかの画像サフィックスが付きます。 また、画像サービングで web サイトを簡単に再調整できるように、ファイルパスのように見えるより複雑な文字列になる場合もあります。

## プロパティ {#id-properties}

テキスト文字列 必須。 画像データテーブルのプライマリインデックスキー。 各 catalog::Id 値は、テーブル内で一意である必要があります。

## 初期設定 {#id-default}

なし

## 関連項目 {#id-seealso}

[attribute::RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)
