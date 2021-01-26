---
description: 検索結果から除外する生成エンジンおよび生成されたアセットタイプを決定します。
seo-description: 検索結果から除外する生成エンジンおよび生成されたアセットタイプを決定します。
seo-title: ExcludeByproductCondition
solution: Experience Manager
title: ExcludeByproductCondition
topic: Dynamic Media Image Production System API
uuid: 70581512-7b26-4319-b12b-27fbb205d871
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 8%

---


# ExcludeByproductCondition{#excludebyproductcondition}

検索結果から除外する生成エンジンおよび生成されたアセットタイプを決定します。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`エンジン`*` | `xsd:string` | 除外するアセットを作成した生成エンジン。 値については、生成情報を参照してください。 |
| `*`generatedAssetType`*` | `xsd:string` | 除外されるアセットタイプ。 値については、アセットタイプを参照してください。 |

