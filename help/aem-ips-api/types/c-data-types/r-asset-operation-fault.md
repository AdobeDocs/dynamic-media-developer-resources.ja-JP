---
description: バッチアセット操作中に生成される警告またはエラーの状態に関する情報が含まれます。 コードと理由のフィールドは、同等の非バッチ操作でスローされたフォルトメッセージフィールドに対応します。
solution: Experience Manager
title: AssetOperationFault
feature: Dynamic Mediaクラシック，SDK/API，アセット管理
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 7%

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

