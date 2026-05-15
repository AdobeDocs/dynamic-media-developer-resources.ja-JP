---
description: デフォルトの応答画像： 画像ファイルが見つからず、defaultImage=がリクエストで指定されていない場合に使用する画像またはカタログエントリを指定します。
solution: Experience Manager
title: DefaultImage
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2044b447-0ee1-4964-b751-8637c5e115d1
TQID: 'https://experienceleague.adobe.com/UcxsxmZBxozuJJh6FdBk-y166UZucXkbPbgfrS5ezEg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 171
ht-degree: 1%

---

# DefaultImage{#defaultimage}

デフォルトの応答画像： 画像ファイルが見つからず、defaultImage=がリクエストで指定されていない場合に使用する画像またはカタログエントリを指定します。

カタログエントリ（テンプレートを含む）または相対パス（`attribute::RootPath`）または絶対イメージファイルパスのいずれかです。 欠落している画像をデフォルトの画像で置き換えるのに便利です。

## プロパティ {#section-b6d8193827c34e5f948792aba8b8daaf}

テキスト文字列。 指定する場合は、この画像カタログの有効な`catalog::Id`値、または画像サーバーがアクセスできる画像ファイルの相対パス（`attribute::RootPath`）または絶対パスである必要があります。

## 制限 {#section-5d8ea872f0b0415fbd3a83410bbcf512}

外部の画像ソースは、デフォルトの画像メカニズムではカバーされません。外部の画像ソースが無効な場合は、エラーが返されます。

## 初期設定 {#section-d88bc8fc71bd413e8f70281d57e1ba1c}

定義されていない場合、`default::DefaultImage`から継承されます。 定義されていても空の場合、`default::DefaultImage`が定義されていても、デフォルトの画像動作は無効になります。

## 関連項目 {#section-dc0fb4e72294442882b33a479fbc2b82}

[属性：:DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782)、[defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)、[属性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)、[ カタログ：:Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)、[属性：:ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)、[属性：:DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)
