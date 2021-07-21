---
description: searchAssetsから返されるメタデータフィールド。
solution: Experience Manager
title: メタデータ
feature: Dynamic Media Classic,SDK/API，メタデータ
role: Developer,Admin
exl-id: 62e3e215-31ea-49fd-937e-d136fdf84aff
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 12%

---

# メタデータ{#metadata}

searchAssetsから返されるメタデータフィールド。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`name`*` | `xsd:string` | メタデータ名。 |
| `*`value`*` | `xsd:string` | メタデータ値。 |
| `*`boolVal`*` | `xsd:boolean` | ブール型メタデータ値（ブール型フィールドのみ）。 |
| `*`longVal`*` | `xsd:long` | 長いメタデータ値（整数型フィールドのみ）。 |
| `*`doubleVal`*` | `xsd:double` | 二重メタデータ値（浮動小数値型フィールドのみ） |
| `*`dateVal`*` | `xsd:dateTime` | 日付メタデータ値（日付型フィールドのみ） |
