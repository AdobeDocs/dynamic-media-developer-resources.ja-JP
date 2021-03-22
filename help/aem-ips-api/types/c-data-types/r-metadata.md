---
description: searchAssetsによって返されるメタデータフィールド。
seo-description: searchAssetsによって返されるメタデータフィールド。
seo-title: メタデータ
solution: Experience Manager
title: メタデータ
uuid: fb7a0ef8-a16c-41e3-84cf-160602cb284b
feature: Dynamic Mediaクラシック，SDK/API，メタデータ
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 12%

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

