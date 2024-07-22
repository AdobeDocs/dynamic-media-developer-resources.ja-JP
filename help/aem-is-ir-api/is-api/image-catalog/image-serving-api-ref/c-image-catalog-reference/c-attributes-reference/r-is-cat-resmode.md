---
title: ResMode
description: デフォルトの再サンプリングモード。 画像データの拡大縮小に使用するデフォルトの再サンプリングおよび補間属性を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a604e61e-be38-4819-b5c3-a79843c1678f
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 3%

---

# ResMode{#resmode}

デフォルトの再サンプリングモード。 画像データの拡大縮小に使用するデフォルトの再サンプリングおよび補間属性を指定します。

`resMode=` がリクエスト内で指定されていない場合に使用されます。

## プロパティ {#section-493f900be522486f97710cebdc4460c2}

列挙値。 補間モードが `bilin` の場合は 2、`bicub` の場合は 3、`sharp2` の場合は 4 に設定します（詳しくは [resMode=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-resmode.md) を参照）。 `sharp` （1）は非推奨（廃止予定）です。 最適な結果を得るには、の代わりに `sharp2` （4）を使用します。

## 初期設定 {#section-35f980e745fc4d79a2621e8abacc724d}

定義されていない場合または空の場合は `default::ResMode` から継承します。

## 関連項目 {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
