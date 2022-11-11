---
description: アセットまたはフォルダーのディスク容量の統計。
solution: Experience Manager
title: DiskUsage
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a3c4c1cd-0fcc-4e7a-a4aa-884d0ce2f208
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 14%

---

# [!DNL DiskUsage]{#diskusage}

アセットまたはフォルダーのディスク容量の統計。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| companyHandle | `xsd:string` | 会社の取り扱い。 |
| companyName | `xsd:string` | 会社名. |
| imageCount | `xsd:int` | 保存されている画像の数。 |
| diskSpaceUsage | `xsd:long` | 合計ファイルサイド (KB)。 |
| lastModified | `xsd:dateTime` | 日付、時刻、およびタイムゾーン `DiskUsage` タイプが最後に変更されました。 |
