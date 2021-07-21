---
description: アセットまたはフォルダーのディスク容量の統計。
solution: Experience Manager
title: DiskUsage
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: a3c4c1cd-0fcc-4e7a-a4aa-884d0ce2f208
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 12%

---

# DiskUsage{#diskusage}

アセットまたはフォルダーのディスク容量の統計。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 会社の担当。 |
| `*`companyName`*` | `xsd:string` | 会社名. |
| `*`imageCount`*` | `xsd:int` | 保存する画像の数。 |
| `*`diskSpaceUsage`*` | `xsd:long` | ファイルサイドの合計(KB)。 |
| `*`lastModified`*` | `xsd:dateTime` | `DiskUsage`タイプが最後に変更された日付、時刻、タイムゾーン。 |
