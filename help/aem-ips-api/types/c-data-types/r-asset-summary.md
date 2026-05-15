---
title: AssetSummary
description: アセットに関する要約された情報を含むメタデータの検索結果。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 25f16a2b-6cd8-485f-a6bd-2a9bc9b3243b
TQID: 'https://experienceleague.adobe.com/RHT8NJiS0pGKUcrYGBsSI1vewvRGUCZmsPYP6Pb0OBs'
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
source-wordcount: 125
ht-degree: 9%

---

# [!DNL AssetSummary]{#assetsummary}

アセットに関する要約された情報を含むメタデータの検索結果。

構文

## パラメーター {#section-ebc75cc024d94c439260d2e71873cc74}

| 名前 | 種類 | 説明 |
|---|---|---|
| assetHandle | `xsd:string` | アセットのハンドル： |
| タイプ | `xsd:string` | アセットタイプ： 「Asset Types」定数は、指定できる値を定義します。 オプション。 |
| name | `xsd:string` | アセット名。 オプション。 |
| フォルダ | `xsd:string` | アセットを含むフォルダー。 |
| ファイル名 | `xsd:string` | アセットのファイル名。 |
| 作成 | `xsd:dateTime` | アセットの作成日： |
| createUser | `xsd:string` | アセットを作成したユーザー |
| lastModified | `xsd:dateTime` | アセットが最後に更新された日付。 |
| lastModifyUser | `xsd:string` | アセットを最後に変更したユーザー。 |
| metadataArray | `types:MetadataArray` | アセットに関連付けられたメタデータ値の配列。 |
| スコア | `xsd:double` | 類似性検索がある場合の精度を定義します（0 =一致なし、1 =完全一致）。 |
| scoreDetail | `xsd:string` | 類似性検索の結果として、類似領域に関する詳細な情報が保持されます。 |
