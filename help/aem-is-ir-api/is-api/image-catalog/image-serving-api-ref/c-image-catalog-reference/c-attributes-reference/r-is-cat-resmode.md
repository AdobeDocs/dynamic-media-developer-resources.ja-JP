---
description: デフォルトの再サンプリングモード。 画像データの拡大縮小に使用するデフォルトの再サンプリングおよび補間属性を指定します。
solution: Experience Manager
title: ResMode
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: a604e61e-be38-4819-b5c3-a79843c1678f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 6%

---

# ResMode{#resmode}

デフォルトの再サンプリングモード。 画像データの拡大縮小に使用するデフォルトの再サンプリングおよび補間属性を指定します。

リクエストで`resMode=`が指定されていない場合に使用されます。

## プロパティ {#section-493f900be522486f97710cebdc4460c2}

列挙 `bilin`の場合は2、`bicub`の場合は3、`sharp2`の場合は4に設定します（詳しくは、` [resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)`を参照）。 `sharp` (1)は非推奨（廃止予定）となりました。最良の結果を得るには、代わりに`sharp2` (4)を使用してください。

## 初期設定 {#section-35f980e745fc4d79a2621e8abacc724d}

`default::ResMode`から継承されます（定義されていない場合または空の場合）。

## 関連項目 {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
