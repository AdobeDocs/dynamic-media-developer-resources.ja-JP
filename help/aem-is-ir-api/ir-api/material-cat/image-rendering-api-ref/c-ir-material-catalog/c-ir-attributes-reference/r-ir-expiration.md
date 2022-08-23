---
title: 有効期限
description: デフォルトのクライアントキャッシュの有効期間。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6d9cca06-f675-4ae4-a187-9cd716e7c554
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 5%

---

# 有効期限{#expiration}

デフォルトのクライアントキャッシュの有効期間。 特定のカタログレコードに有効な `catalog::Expiration` または `vignette::Expiration` の値です。 または、ビネットファイルまたはマテリアルファイルに、カタログレコードを介してではなく、直接アクセスする場合。

## プロパティ {#section-8e2bade105ec4905ae5c4911f500279f}

実数 `0` 以上 返信データが生成されてから有効期限が切れるまでの時間数。 に設定 `0` 常に返信画像を即座に期限切れにする。これにより、クライアントのキャッシュが効果的に無効になります。 に設定 `-1` 印を付ける *無期限*.

## 初期設定 {#section-18cfce46edb441bfae7dd9d3e0217ba9}

継承元 `default::Expiration` が定義されていない場合、または空の場合は。

## 関連項目 {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) , [vignette::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)
