---
description: PostScriptファイルのプロパティ。
seo-description: PostScriptファイルのプロパティ。
seo-title: GenerationInfo
solution: Experience Manager
title: GenerationInfo
topic: Scene7 Image Production System API
uuid: 166637e5-b981-4f64-8d92-5fce4f1b20d2
translation-type: tm+mt
source-git-commit: 55015831ed1971a305ddbd8085c95626507355e0
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 13%

---


# GenerationInfo{#generationinfo}

PostScriptファイルのプロパティ。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| ` *`エンジン`*` | `xsd:string` | 使用される生成エンジン（値については「生成情報」を参照）。 |
| ` *`原始者`*` | `types:Asset` | 生成で使用される主要資産の資産レコード。 |
| ` *`生成`*` | `types:Asset` | 生成されたアセットのアセットレコード。 |
| ` *`attributeArray`*` | `types:GenerationAttributeArray` | 生成プロセスに関連付けられた属性の配列。 |

