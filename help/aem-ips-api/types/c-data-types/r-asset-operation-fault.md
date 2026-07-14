---
title: AssetOperationFault
description: バッチアセットの操作中に生成される警告またはエラー条件に関する情報が含まれます。 コード フィールドと理由フィールドは、同等の非バッチ操作のためにスローされたフォールトメッセージフィールドに対応します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
TQID: 'https://experienceleague.adobe.com/LCiMAp-8grDIfCEGX3sF2kBhDamlxZ8iFHT1BjBLkCY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 92
ht-degree: 6%

---

# [!DNL AssetOperationFault]{#assetoperationfault}

バッチアセットの操作中に生成される警告またはエラー条件に関する情報が含まれます。 コード フィールドと理由フィールドは、同等の非バッチ操作のためにスローされたフォールトメッセージフィールドに対応します。

構文

## パラメーター {#section-c906f052f43e4785ba46d92b514b0923}

| 名前 | 種類 | 説明 |
|---|---|---|
| assetHandle | `xsd:string` | 失敗した操作のアセットハンドル。 |
| コード | `xsd:int` | 操作の障害コード |
| 理由 | `xsd:string` | エラーの説明または理由。 |

