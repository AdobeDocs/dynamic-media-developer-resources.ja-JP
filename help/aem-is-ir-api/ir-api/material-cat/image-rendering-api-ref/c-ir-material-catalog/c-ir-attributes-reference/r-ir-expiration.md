---
description: デフォルトのクライアントキャッシュの有効期間。 特定のカタログレコードに有効なカタログの有効期限またはビネットの有効期限の値が含まれていない場合や、ビネットファイルまたはマテリアルファイルにカタログレコード経由ではなく直接アクセスする場合に、既定の有効期限を指定します。
solution: Experience Manager
title: 有効期限
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 6d9cca06-f675-4ae4-a187-9cd716e7c554
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 3%

---

# 有効期限{#expiration}

デフォルトのクライアントキャッシュの有効期間。 特定のカタログレコードに有効なcatalog::Expirationまたはvignette::Expiration値が含まれていない場合や、ビネットファイルやマテリアルファイルにカタログレコード経由ではなく直接アクセスする場合の、既定の有効期限間隔を指定します。

## プロパティ {#section-8e2bade105ec4905ae5c4911f500279f}

0以上の実数。 応答データが生成されてから有効期限が切れるまでの時間数。 0に設定すると、常に返信イメージの有効期限が即座に切れ、クライアントのキャッシュが効果的に無効になります。 -1に設定すると、*無期限*&#x200B;とマークされます。

## 初期設定 {#section-18cfce46edb441bfae7dd9d3e0217ba9}

default::Expirationから継承されます（定義されていない場合または空の場合）。

## 関連項目 {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) 、 [vignette::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)
