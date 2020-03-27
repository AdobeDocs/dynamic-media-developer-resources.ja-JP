---
description: アセットまたはフォルダーのディスク領域の統計。
seo-description: アセットまたはフォルダーのディスク領域の統計。
seo-title: DiskUsage
solution: Experience Manager
title: DiskUsage
topic: Scene7 Image Production System API
uuid: a63f0ed0-c689-43b0-9c3e-9500715d15a5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# DiskUsage{#diskusage}

アセットまたはフォルダーのディスク領域の統計。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 会社の担当。 |
| ` *`companyName`*` | `xsd:string` | 会社名. |
| ` *`imageCount`*` | `xsd:int` | 保存されている画像の数。 |
| ` *`diskSpaceUsage`*` | `xsd:long` | ファイル側の合計(KB)。 |
| ` *`lastModified`*` | `xsd:dateTime` | タイプが最後に変更された日 `DiskUsage` 付、時刻、タイムゾーン。 |

