---
description: batchSetAssetMetadata操作での使用更新に関する警告またはエラーの詳細。
solution: Experience Manager
title: SetMetadataFault
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 49c6f355-4b5f-4b98-9a58-5732d56fdccb
TQID: 'https://experienceleague.adobe.com/kqC7eTmOZHNIYAn8yTKr-q-rJMQMzqBC9moArFK9no4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 58
ht-degree: 10%

---

# [!DNL SetMetadataFault]{#setmetadatafault}

batchSetAssetMetadata操作での使用更新に関する警告またはエラーの詳細。

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| assetHandle | `xsd:string` | メタデータが正しく設定されなかったアセット。 |
| fieldHandle | `xsd:string` | 値が正しく設定されていないメタデータフィールドへのハンドル。 |
| コード | `xsd:int` | フォールトコード。 |
| 理由 | `xsd:string` | エラーの説明（プレーンテキスト）。 |
