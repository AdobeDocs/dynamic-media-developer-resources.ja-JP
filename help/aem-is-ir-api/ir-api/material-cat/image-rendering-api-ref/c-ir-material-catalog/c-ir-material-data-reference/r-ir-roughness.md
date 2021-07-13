---
description: 表面粗さ。 マテリアルサーフェスの相対光沢度を指定します。 3D反射レンダリング効果を制御するために、カタログの種類とカタログの光沢と組み合わせて使用します。
solution: Experience Manager
title: 粗さ
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 61d956ec-62dd-4879-877e-2ac422396e2e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 3%

---

# 粗さ{#roughness}

表面粗さ。 マテリアルサーフェスの相対光沢度を指定します。 catalog::Typeおよびcatalog::Glossと組み合わせて使用し、3D反射レンダリング効果を制御します。

## プロパティ {#section-70c3f2394fd8477ca83a369448907971}

整数。 0 ～ 100の範囲の割合の値です。 すべての材料に対してオプションです。 複数の反射マップを持つビネット、または3D反射機能を持つビネットにのみ使用されます。 不明な場合や不要な場合は、空のままにするか、-1に設定します。

## 初期設定 {#section-c6d5c0613a8745ddbd9f43c8c90b1580}

-1;サーバーのデフォルト値が使用されます。

## 関連項目 {#section-d08b59eb76824226b89c6fdf86bb5ce5}

[rough=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180) 、 [catalog::Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb)、 [catalog::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
