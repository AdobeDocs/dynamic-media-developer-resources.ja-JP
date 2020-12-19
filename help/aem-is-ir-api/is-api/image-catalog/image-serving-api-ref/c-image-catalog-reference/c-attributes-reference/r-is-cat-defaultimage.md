---
description: 初期設定の応答画像。 画像ファイルが見つからず、defaultImage=が要求で指定されていない場合に使用する画像またはカタログエントリを指定します。
seo-description: 初期設定の応答画像。 画像ファイルが見つからず、defaultImage=が要求で指定されていない場合に使用する画像またはカタログエントリを指定します。
seo-title: DefaultImage
solution: Experience Manager
title: DefaultImage
topic: Scene7 Image Serving - Image Rendering API
uuid: 6f8f50af-15bb-4333-b227-3eba38653a7d
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 2%

---


# DefaultImage{#defaultimage}

初期設定の応答画像。 画像ファイルが見つからず、defaultImage=が要求で指定されていない場合に使用する画像またはカタログエントリを指定します。

カタログエントリ（テンプレートを含む）、相対パス(`attribute::RootPath`)、または画像の絶対パスを指定できます。 見つからない画像を初期設定の画像に置き換える場合に便利です。

## プロパティ {#section-b6d8193827c34e5f948792aba8b8daaf}

テキスト文字列。 指定する場合、この画像カタログ内の有効な`catalog::Id`値、またはImage Serverがアクセス可能な画像ファイルの相対パス（`attribute::RootPath`から）または絶対パスで指定する必要があります。

## 制限{#section-5d8ea872f0b0415fbd3a83410bbcf512}

外部画像ソースは、初期設定の画像メカニズムではカバーされません。外部の画像ソースが有効でない場合は、エラーが返されます。

## 初期設定 {#section-d88bc8fc71bd413e8f70281d57e1ba1c}

定義されていない場合は`default::DefaultImage`から継承されます。 定義済みで空の場合、`default::DefaultImage`が定義されている場合でも、初期設定の画像動作は無効になります。

## 関連項目 {#section-dc0fb4e72294442882b33a479fbc2b82}

[attribute::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) ,  [defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [attribute::RootPath, ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)catalog:Id:Id [, Image](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md):ErrorErrorError, default Attribute::DefaultImage=,  [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c) [attribute::RootPath, Catalog:Atalog:](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)
