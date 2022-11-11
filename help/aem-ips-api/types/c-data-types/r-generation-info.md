---
description: PostScript ファイルのプロパティ。
solution: Experience Manager
title: GenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9aac2973-bbcb-4914-9bf9-203f0357527c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '45'
ht-degree: 11%

---

# [!DNL GenerationInfo]{#generationinfo}

PostScript ファイルのプロパティ。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| [!DNL engine] | `xsd:string` | 使用された生成エンジン（値については「生成情報」を参照）。 |
| [!DNL originator] | `types:Asset` | 生成で使用されるプライマリアセットのアセットレコード。 |
| [!DNL generated] | `types:Asset` | 生成されたアセットのアセットレコード。 |
| attributeArray | `types:GenerationAttributeArray` | 生成プロセスに関連付けられた属性の配列。 |
