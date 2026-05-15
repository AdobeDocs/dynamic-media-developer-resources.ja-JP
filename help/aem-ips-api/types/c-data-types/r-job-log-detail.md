---
description: ジョブのログ情報：
solution: Experience Manager
title: JobLogDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fe41a48a-4671-4179-a128-aadc7bc0683b
TQID: 'https://experienceleague.adobe.com/wH0F5TxaTHxn-vP7PTri94WxEa5Bs9Q2-CRnuHdVb3I'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 60
ht-degree: 6%

---

# [!DNL JobLogDetail]{#joblogdetail}

ジョブのログ情報：

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| logMessage | `xsd:string` | ジョブのログにメッセージが記録されます。 |
| logType | `xsd:string` | ジョブのログファイルの種類。 |
| assetName | `xsd:string` | ジョブログ内のアセットの名前（オプション）。 |
| assetType | `xsd:string` | アセットタイプの選択。 |
| assetHandle | `xsd:string` | ジョブログでアセットハンドルが参照されています。 |
| auxArray | `types:JobLogDetailAuxArray` | 上記の5つのジョブログタイプ以外の詳細なジョブログ情報を提供します。 |
