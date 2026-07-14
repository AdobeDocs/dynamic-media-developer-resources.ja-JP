---
description: アセットまたはフォルダーのディスク領域の統計情報。
solution: Experience Manager
title: DiskUsage
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a3c4c1cd-0fcc-4e7a-a4aa-884d0ce2f208
TQID: 'https://experienceleague.adobe.com/Md0oAgpJDqSrn1JRZsebpaZKeXIAoLcgkC5KPaHad5s'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 50
ht-degree: 8%

---

# [!DNL DiskUsage]{#diskusage}

アセットまたはフォルダーのディスク領域の統計情報。

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| companyHandle | `xsd:string` | 会社のハンドル。 |
| companyName | `xsd:string` | 企業名。 |
| imageCount | `xsd:int` | 保存された画像の数。 |
| diskSpaceUsage | `xsd:long` | ファイルサイドの合計（キロバイト）。 |
| lastModified | `xsd:dateTime` | `DiskUsage` タイプが最後に変更された日付、時刻、およびタイムゾーン。 |

