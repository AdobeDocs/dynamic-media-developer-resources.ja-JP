---
description: バッチアセット操作中に生成される警告またはエラーの状態に関する情報が含まれます。 コードと理由のフィールドは、同等の非バッチ操作でスローされたフォルトメッセージフィールドに対応します。
seo-description: バッチアセット操作中に生成される警告またはエラーの状態に関する情報が含まれます。 コードと理由のフィールドは、同等の非バッチ操作でスローされたフォルトメッセージフィールドに対応します。
seo-title: AssetOperationFault
solution: Experience Manager
title: AssetOperationFault
topic: Dynamic Media Image Production System API
uuid: fb6c5482-6e16-4561-927b-e4daeb7bdd7b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 5%

---


# AssetOperationFault{#assetoperationfault}

バッチアセット操作中に生成される警告またはエラーの状態に関する情報が含まれます。 コードと理由のフィールドは、同等の非バッチ操作でスローされたフォルトメッセージフィールドに対応します。

構文

## パラメータ {#section-c906f052f43e4785ba46d92b514b0923}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 失敗した操作のアセットハンドル。 |
| `*`コード`*` | `xsd:int` | 操作のエラーコード。 |
| `*`理由`*` | `xsd:string` | 障害の説明または理由。 |

