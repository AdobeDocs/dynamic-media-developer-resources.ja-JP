---
description: searchAssetsによって返されるメタデータフィールド。
seo-description: searchAssetsによって返されるメタデータフィールド。
seo-title: メタデータ
solution: Experience Manager
title: メタデータ
topic: Dynamic Media Image Production System API
uuid: fb7a0ef8-a16c-41e3-84cf-160602cb284b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 14%

---


# メタデータ{#metadata}

searchAssetsによって返されるメタデータフィールド。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`name`*` | `xsd:string` | メタデータ名。 |
| `*`value`*` | `xsd:string` | メタデータ値。 |
| `*`boolVal`*` | `xsd:boolean` | ブール型メタデータ値（ブール型フィールドのみ） |
| `*`longVal`*` | `xsd:long` | 長いメタデータ値（整数型フィールドのみ） |
| `*`doubleVal`*` | `xsd:double` | 重複のメタデータ値（浮動小数点数型のフィールドのみ） |
| `*`dateVal`*` | `xsd:dateTime` | 日付メタデータ値（日付を入力したフィールドのみ） |

