---
description: アセットまたはフォルダーのディスク領域の統計。
seo-description: アセットまたはフォルダーのディスク領域の統計。
seo-title: DiskUsage
solution: Experience Manager
title: DiskUsage
topic: Dynamic Media Image Production System API
uuid: a63f0ed0-c689-43b0-9c3e-9500715d15a5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 11%

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

