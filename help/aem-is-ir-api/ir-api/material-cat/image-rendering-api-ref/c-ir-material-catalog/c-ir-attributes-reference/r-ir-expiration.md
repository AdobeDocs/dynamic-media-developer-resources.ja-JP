---
description: デフォルトのクライアントキャッシュの有効時間。 特定のカタログレコードに有効なカタログの有効期限またはビネットの有効期限の値が含まれていない場合や、ビネットファイルやマテリアルファイルがカタログレコードを経由せずに直接アクセスされる場合に、初期設定の有効期限の間隔を指定します。
seo-description: デフォルトのクライアントキャッシュの有効時間。 特定のカタログレコードに有効なカタログの有効期限またはビネットの有効期限の値が含まれていない場合や、ビネットファイルやマテリアルファイルがカタログレコードを経由せずに直接アクセスされる場合に、初期設定の有効期限の間隔を指定します。
seo-title: 有効期限
solution: Experience Manager
title: 有効期限
topic: Scene7 Image Serving - Image Rendering API
uuid: 2b56f9ec-2b25-4e6a-aead-6dad3d2df975
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 有効期限{#expiration}

デフォルトのクライアントキャッシュの有効時間。 特定のカタログレコードに有効なcatalog::Expirationまたはvignette::Expiration値が含まれていない場合や、ビネットファイルまたはマテリアルファイルがカタログレコードを介してではなく直接アクセスされた場合に、初期設定の有効期限間隔を指定します。

## プロパティ {#section-8e2bade105ec4905ae5c4911f500279f}

0以上の実数。 応答データが生成されてから有効期限切れになるまでの時間数。 0に設定すると、常に応答イメージの有効期限が直ちに切れます。これにより、クライアントのキャッシュが事実上無効になります。 -1に設定すると、無期限としてマ *ークされます*。

## 初期設定 {#section-18cfce46edb441bfae7dd9d3e0217ba9}

default::Expirationから継承（定義されていない場合または空の場合）。

## 関連項目 {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) , [vignette::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)
