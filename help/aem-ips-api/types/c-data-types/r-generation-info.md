---
description: PostScript ファイルのプロパティ。
solution: Experience Manager
title: GenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9aac2973-bbcb-4914-9bf9-203f0357527c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 14%

---

# GenerationInfo{#generationinfo}

PostScript ファイルのプロパティ。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| エンジン | `xsd:string` | 使用された生成エンジン（値については「生成情報」を参照）。 |
| 作成者 | `types:Asset` | 生成で使用されるプライマリアセットのアセットレコード。 |
| 生成 | `types:Asset` | 生成されたアセットのアセットレコード。 |
| attributeArray | `types:GenerationAttributeArray` | 生成プロセスに関連付けられた属性の配列。 |
