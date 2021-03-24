---
description: 検索結果から除外する生成エンジンおよび生成されたアセットタイプを決定します。
solution: Experience Manager
title: ExcludeByproductCondition
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 9%

---


# ExcludeByproductCondition{#excludebyproductcondition}

検索結果から除外する生成エンジンおよび生成されたアセットタイプを決定します。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`エンジン`*` | `xsd:string` | 除外するアセットを作成した生成エンジン。 値については、生成情報を参照してください。 |
| `*`generatedAssetType`*` | `xsd:string` | 除外されるアセットタイプ。 値については、アセットタイプを参照してください。 |

