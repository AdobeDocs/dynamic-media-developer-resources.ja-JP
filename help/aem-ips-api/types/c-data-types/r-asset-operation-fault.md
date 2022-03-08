---
title: AssetOperationFault
description: バッチアセット操作中に生成された警告またはエラー状態に関する情報が含まれます。 コードおよび理由フィールドは、同等の非バッチ操作でスローされた障害メッセージフィールドに対応しています。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 7%

---

# AssetOperationFault{#assetoperationfault}

バッチアセット操作中に生成された警告またはエラー状態に関する情報が含まれます。 コードおよび理由フィールドは、同等の非バッチ操作でスローされた障害メッセージフィールドに対応しています。

構文

## パラメータ {#section-c906f052f43e4785ba46d92b514b0923}

| 名前 | 種類 | 説明 |
|---|---|---|
| assetHandle | `xsd:string` | 失敗した操作のアセットハンドル。 |
| コード | `xsd:int` | 操作の障害コード。 |
| 理由 | `xsd:string` | 障害の説明または理由。 |
