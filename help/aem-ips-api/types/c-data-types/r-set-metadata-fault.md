---
description: batchSetAssetMetadata 操作での歌の更新に関する警告またはエラーの詳細。
solution: Experience Manager
title: SetMetadataFault
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 49c6f355-4b5f-4b98-9a58-5732d56fdccb
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 10%

---

# [!DNL SetMetadataFault]{#setmetadatafault}

batchSetAssetMetadata 操作での歌の更新に関する警告またはエラーの詳細。

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| assetHandle | `xsd:string` | メタデータが正常に設定されなかったアセット。 |
| fieldHandle | `xsd:string` | 値が正常に設定されなかったメタデータフィールドへのハンドル。 |
| コード | `xsd:int` | 障害コード |
| 理由 | `xsd:string` | 障害の説明（プレーンテキスト）。 |
