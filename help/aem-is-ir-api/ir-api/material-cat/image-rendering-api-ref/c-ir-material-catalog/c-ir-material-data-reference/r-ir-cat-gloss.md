---
description: '[ サーフェス光沢 ] マテリアル サーフェスの相対的な光沢を指定します。'
solution: Experience Manager
title: 光沢
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 72c5d2f9-a7e6-4ad3-aebe-6a1b1fa5453f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 2%

---

# 光沢{#gloss}

[ サーフェス光沢 ] マテリアル サーフェスの相対的な光沢を指定します。

この値は、次の目的でレンダラーによって使用されます。

* `catalog::Illum` が–1 の場合は、照明マップを選択します。
* `catalog::Type` と共に光沢効果（鏡面反射）レンダリングを制御します。
* `catalog::Type` および `catalog::Roughness` と組み合わせて 3D 反射レンダリング効果をコントロールします。

## プロパティ {#section-ddc475c0556f4f67b4cf62bd1bcd4bf7}

整数。 0 ～ 100 の範囲のパーセンテージ数値です。 すべてのマテリアルに対してオプションです。 多重反射マップを持つビネットまたは 3D 反射機能を持つビネットにのみ使用されます。 不明な場合や不要な場合は、空のままにするか、-1 に設定します。

## 初期設定 {#section-2352721073524f1a8d461f64a363aac9}

この値が–1 に設定されている場合、ヴィネットによってデフォルト値が提供されます。

## 関連項目 {#section-0213bbdb7d6d4974a7c53822957717c1}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) , [catalog::Roughness](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99), [catalog::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
