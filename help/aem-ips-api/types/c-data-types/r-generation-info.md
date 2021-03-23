---
description: PostScriptファイルのプロパティ。
seo-description: PostScriptファイルのプロパティ。
seo-title: GenerationInfo
solution: Experience Manager
title: GenerationInfo
uuid: 166637e5-b981-4f64-8d92-5fce4f1b20d2
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 11%

---


# GenerationInfo{#generationinfo}

PostScriptファイルのプロパティ。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`エンジン`*` | `xsd:string` | 使用される生成エンジン（値については「生成情報」を参照）。 |
| `*`原始者`*` | `types:Asset` | 生成で使用される主要資産の資産レコード。 |
| `*`生成`*` | `types:Asset` | 生成されたアセットのアセットレコード。 |
| `*`attributeArray`*` | `types:GenerationAttributeArray` | 生成プロセスに関連付けられた属性の配列。 |

