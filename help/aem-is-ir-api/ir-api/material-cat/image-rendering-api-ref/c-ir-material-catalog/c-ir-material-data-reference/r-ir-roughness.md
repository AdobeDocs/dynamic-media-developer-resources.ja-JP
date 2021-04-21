---
description: 表面粗さ。 マテリアルサーフェスの相対的な光沢を指定します。 カタログの種類とカタログの光沢と組み合わせて使用し、3D反射レンダリング効果を制御します。
solution: Experience Manager
title: 粗さ
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 3%

---


# 粗さ{#roughness}

表面粗さ。 マテリアルサーフェスの相対的な光沢を指定します。 catalog::Typeとcatalog::Glossと組み合わせて使用し、3D反射レンダリング効果を制御します。

## プロパティ {#section-70c3f2394fd8477ca83a369448907971}

整数値。 0 ～ 100の範囲のパーセント値。 すべての材料に対してオプションです。 複数の反射マップを持つビネット、または3D反射機能を持つビネットにのみ使用します。 不明または不要な場合は、空白のままにするか、-1に設定します。

## 初期設定 {#section-c6d5c0613a8745ddbd9f43c8c90b1580}

-1;サーバのデフォルト値が使用されます。

## 関連項目 {#section-d08b59eb76824226b89c6fdf86bb5ce5}

[rough=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180) ,  [catalog::Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb),  [catalog::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
