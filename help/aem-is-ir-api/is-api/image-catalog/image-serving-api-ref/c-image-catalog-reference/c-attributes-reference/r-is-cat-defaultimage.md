---
description: デフォルトの応答画像。 画像ファイルが見つからず、defaultImage=がリクエストで指定されていない場合に使用する画像またはカタログエントリを指定します。
solution: Experience Manager
title: DefaultImage
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2044b447-0ee1-4964-b751-8637c5e115d1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

---

# DefaultImage{#defaultimage}

デフォルトの応答画像。 画像ファイルが見つからず、defaultImage=がリクエストで指定されていない場合に使用する画像またはカタログエントリを指定します。

カタログエントリ（テンプレートを含む）、相対パス（`attribute::RootPath` に対する）、または画像ファイルパスの絶対パスのいずれかを指定できます。 不足している画像をデフォルトの画像に置き換える場合に役立ちます。

## プロパティ {#section-b6d8193827c34e5f948792aba8b8daaf}

テキスト文字列 指定する場合、は、この画像カタログ内の有効な `catalog::Id` 値、または Image Server からアクセス可能な画像ファイルへの相対パス（`attribute::RootPath` に対する相対パス）または絶対パスである必要があります。

## 制限 {#section-5d8ea872f0b0415fbd3a83410bbcf512}

外部の画像ソースはデフォルトの画像メカニズムでカバーされません。外部の画像ソースが有効でない場合はエラーが返されます。

## 初期設定 {#section-d88bc8fc71bd413e8f70281d57e1ba1c}

定義されていない場合は `default::DefaultImage` から継承します。 定義されていても空の場合、`default::DefaultImage` が定義されていても、デフォルトの画像動作は無効になります。

## 関連項目 {#section-dc0fb4e72294442882b33a479fbc2b82}

[attribute::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782)、[defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)、[attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)、[catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)、[attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)、[attribute::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)
