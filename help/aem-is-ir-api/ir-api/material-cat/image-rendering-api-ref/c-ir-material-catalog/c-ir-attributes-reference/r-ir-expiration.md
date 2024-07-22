---
title: 有効期限
description: デフォルトのクライアントキャッシュの有効期限。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6d9cca06-f675-4ae4-a187-9cd716e7c554
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 4%

---

# 有効期限{#expiration}

デフォルトのクライアントキャッシュの有効期限。 特定のカタログレコードに有効な `catalog::Expiration` または `vignette::Expiration` 値が含まれていない場合に使用する、デフォルトの有効期限間隔を指定します。 または、ビネット ファイルまたはマテリアル ファイルに、カタログ レコード経由ではなく直接アクセスする場合です。

## プロパティ {#section-8e2bade105ec4905ae5c4911f500279f}

`0` 以上の実数。 返信データが生成されてから有効期限が切れるまでの時間数。 返信画像を常にすぐに有効期限切れにする場合は `0` に設定します。これにより、クライアントのキャッシュが効果的に無効になります。 `-1` に設定すると、*有効期限切れになりません* としてマークされます。

## 初期設定 {#section-18cfce46edb441bfae7dd9d3e0217ba9}

定義されていない場合または空の場合は `default::Expiration` から継承します。

## 関連項目 {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) , [vignette::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)
