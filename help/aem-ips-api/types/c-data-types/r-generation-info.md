---
description: PostScriptファイルのプロパティ。
solution: Experience Manager
title: GenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 12%

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

