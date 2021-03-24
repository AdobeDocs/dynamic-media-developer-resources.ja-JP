---
description: アセットまたはフォルダーのディスク領域の統計。
solution: Experience Manager
title: DiskUsage
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 12%

---


# DiskUsage{#diskusage}

アセットまたはフォルダーのディスク領域の統計。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 会社ハンドル |
| `*`companyName`*` | `xsd:string` | 会社名. |
| `*`imageCount`*` | `xsd:int` | 保存されている画像の数。 |
| `*`diskSpaceUsage`*` | `xsd:long` | ファイル側の合計(KB)。 |
| `*`lastModified`*` | `xsd:dateTime` | `DiskUsage`型の日付、時刻、およびタイムゾーンが最後に変更されました。 |

