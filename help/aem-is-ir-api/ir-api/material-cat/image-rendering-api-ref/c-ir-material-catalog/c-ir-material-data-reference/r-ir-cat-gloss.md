---
description: サーフェスの光沢度マテリアル サーフェスの相対的な光沢度を指定します。
solution: Experience Manager
title: 光沢
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 72c5d2f9-a7e6-4ad3-aebe-6a1b1fa5453f
TQID: 'https://experienceleague.adobe.com/Q1mOPjFXFnSPVRsvYpKs3a-15g1BfxQRCsFaMRBZNTw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 121
ht-degree: 2%

---

# 光沢{#gloss}

サーフェスの光沢度マテリアル サーフェスの相対的な光沢度を指定します。

この値は、次の目的のためにレンダラーで使用されます。

* `catalog::Illum`が–1の場合は、照明マップを選択します。
* 光沢効果（スペキュラ リフレクション）のレンダリングを`catalog::Type`と組み合わせて制御します。
* `catalog::Type`および`catalog::Roughness`と組み合わせて3D リフレクションレンダーエフェクトを制御します。

## プロパティ {#section-ddc475c0556f4f67b4cf62bd1bcd4bf7}

整数。 0...100の範囲内のパーセント数。 すべてのマテリアルに対してオプションです。 複数のリフレクションマップを持つビネットまたは3D リフレクション機能を持つビネットにのみ使用します。 不明な場合や不要な場合は、空のままにするか、-1に設定します。

## 初期設定 {#section-2352721073524f1a8d461f64a363aac9}

デフォルト値は、この値が–1に設定されている場合に周辺光量補正によって提供されます。

## 関連項目 {#section-0213bbdb7d6d4974a7c53822957717c1}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)、[ カタログ：:Roughness](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99)、[ カタログ：:Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
