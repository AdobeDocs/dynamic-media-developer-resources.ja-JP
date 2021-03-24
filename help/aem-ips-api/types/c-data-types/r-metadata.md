---
description: searchAssetsによって返されるメタデータフィールド。
solution: Experience Manager
title: メタデータ
feature: Dynamic Mediaクラシック，SDK/API，メタデータ
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '65'
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

