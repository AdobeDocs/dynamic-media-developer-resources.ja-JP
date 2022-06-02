---
title: ResMode
description: 初期設定の再サンプリングモード。 画像データの拡大/縮小に使用する初期設定の再サンプリングおよび補間属性を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a604e61e-be38-4819-b5c3-a79843c1678f
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 6%

---

# ResMode{#resmode}

初期設定の再サンプリングモード。 画像データの拡大/縮小に使用する初期設定の再サンプリングおよび補間属性を指定します。

次の場合に使用 `resMode=` がリクエストで指定されていません。

## プロパティ {#section-493f900be522486f97710cebdc4460c2}

列挙。 の 2 に設定 `bilin`, 3 の場合 `bicub`、または 4 `sharp2` 補間モード ( [resMode=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-resmode.md) を参照 )。 `sharp` (1) は廃止されています。 用途 `sharp2` (4) を使用します。

## 初期設定 {#section-35f980e745fc4d79a2621e8abacc724d}

継承元 `default::ResMode` が定義されていない場合、または空の場合は。

## 関連項目 {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
