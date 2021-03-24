---
description: 初期設定の再サンプリングモード。 画像データのスケールに使用する初期設定のリサンプリング属性と補間属性を指定します。
solution: Experience Manager
title: ResMode
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 5%

---


# ResMode{#resmode}

初期設定の再サンプリングモード。 画像データのスケールに使用する初期設定のリサンプリング属性と補間属性を指定します。

リクエストで`resMode=`が指定されていない場合に使用されます。

## プロパティ {#section-493f900be522486f97710cebdc4460c2}

列挙。 `bilin`の場合は2、`bicub`の場合は3、`sharp2`の場合は4に設定します（詳しくは` [resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)`を参照）。 `sharp` (1)は非推奨です。最良の結果を得るには、代わりに`sharp2` (4)を使用します。

## 初期設定 {#section-35f980e745fc4d79a2621e8abacc724d}

定義されていない場合や空の場合は`default::ResMode`から継承されます。

## 関連項目 {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
