---
title: AssetOperationFault
description: アセットのバッチ操作中に生成された警告またはエラーの状態に関する情報が含まれます。 「コード」フィールドと「理由」フィールドは、同等の非バッチ操作のためにスローされる障害メッセージフィールドに対応しています。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 6%

---

# [!DNL AssetOperationFault]{#assetoperationfault}

アセットのバッチ操作中に生成された警告またはエラーの状態に関する情報が含まれます。 「コード」フィールドと「理由」フィールドは、同等の非バッチ操作のためにスローされる障害メッセージフィールドに対応しています。

構文

## パラメーター {#section-c906f052f43e4785ba46d92b514b0923}

| 名前 | 種類 | 説明 |
|---|---|---|
| assetHandle | `xsd:string` | 失敗した操作のアセットハンドル。 |
| コード | `xsd:int` | 操作のエラーコード。 |
| 理由 | `xsd:string` | 障害の説明または理由。 |
