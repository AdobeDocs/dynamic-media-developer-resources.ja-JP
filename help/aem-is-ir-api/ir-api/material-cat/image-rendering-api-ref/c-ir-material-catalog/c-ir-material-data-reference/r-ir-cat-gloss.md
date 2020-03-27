---
description: '[サーフェス光沢]マテリアルサーフェスの相対的な光沢を指定します。'
seo-description: '[サーフェス光沢]マテリアルサーフェスの相対的な光沢を指定します。'
seo-title: 光沢
solution: Experience Manager
title: 光沢
topic: Scene7 Image Serving - Image Rendering API
uuid: 7db83f99-15ab-4c43-adfb-07ad0b0c9707
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 光沢{#gloss}

[サーフェス光沢]マテリアルサーフェスの相対的な光沢を指定します。

この値は、次の目的でレンダラーによって使用されます。

* が —1の場合は、イルミネーションマ `catalog::Illum` ップを選択します。
* と組み合わせて光沢効果（鏡面反射）のレンダリングを制御しま `catalog::Type`す。
* と組み合わせて3D反射レンダリング効果を制 `catalog::Type` 御しま `catalog::Roughness`す。

## プロパティ {#section-ddc475c0556f4f67b4cf62bd1bcd4bf7}

整数。 0 ～ 100の範囲のパーセント値。 すべてのマテリアルのオプションです。 複数の反射マップを持つビネットまたは3D反射機能を持つビネットにのみ使用されます。 不明な場合や不要な場合は、空のままにするか、-1に設定します。

## 初期設定 {#section-2352721073524f1a8d461f64a363aac9}

ビネットで —1に設定されている場合、デフォルト値が提供されます。

## 関連項目 {#section-0213bbdb7d6d4974a7c53822957717c1}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) , [catalog::Roughness](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99), [catalog::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
