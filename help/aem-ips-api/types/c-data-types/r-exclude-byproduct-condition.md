---
description: 検索結果から除外する生成エンジンと生成されたアセットタイプを決定します。
solution: Experience Manager
title: ExcludeByproductCondition
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 5b37e01b-9e9c-4d34-9d39-1f9bfe356e53
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 9%

---

# ExcludeByproductCondition{#excludebyproductcondition}

検索結果から除外する生成エンジンと生成されたアセットタイプを決定します。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`エンジン`*` | `xsd:string` | 除外するアセットを作成した生成エンジン。 値については、生成情報を参照してください。 |
| `*`generatedAssetType`*` | `xsd:string` | 除外されたアセットタイプ。 値については、アセットタイプを参照してください。 |
