---
description: searchAssets から返されるメタデータフィールド。
solution: Experience Manager
title: メタデータ
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 62e3e215-31ea-49fd-937e-d136fdf84aff
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 12%

---

# [!DNL Metadata]{#metadata}

searchAssets から返されるメタデータフィールド。

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| name | `xsd:string` | メタデータ名。 |
| value | `xsd:string` | メタデータ値。 |
| boolVal | `xsd:boolean` | ブール型メタデータ値（ブール型入力フィールドのみ） |
| longVal | `xsd:long` | 長いメタデータ値（整数タイプのフィールドのみ）。 |
| doubleVal | `xsd:double` | ダブルメタデータ値（float 型フィールドのみ）。 |
| dateVal | `xsd:dateTime` | 日付メタデータ値（日付型フィールドのみ）。 |
