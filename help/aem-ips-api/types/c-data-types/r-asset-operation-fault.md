---
description: バッチアセット操作中に生成された警告またはエラーの状態に関する情報が含まれます。 コードと理由のフィールドは、同等の非バッチ操作でスローされたフォルトメッセージフィールドに対応します。
solution: Experience Manager
title: AssetOperationFault
feature: Dynamic Media Classic,SDK/API，アセット管理
role: Developer,Admin
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 7%

---

# AssetOperationFault{#assetoperationfault}

バッチアセット操作中に生成された警告またはエラーの状態に関する情報が含まれます。 コードと理由のフィールドは、同等の非バッチ操作でスローされたフォルトメッセージフィールドに対応します。

構文

## パラメータ {#section-c906f052f43e4785ba46d92b514b0923}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 失敗した操作のアセットハンドル。 |
| `*`コード`*` | `xsd:int` | 操作の障害コード。 |
| `*`理由`*` | `xsd:string` | 障害の説明または理由。 |
