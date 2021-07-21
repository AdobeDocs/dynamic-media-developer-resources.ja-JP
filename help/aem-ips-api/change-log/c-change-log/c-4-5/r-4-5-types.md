---
description: IPS APIバージョン4.5の新しいデータ型と変更されたデータ型について説明します。
solution: Experience Manager
title: 新規および変更されたデータタイプ
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 45024d75-8058-40f8-b3e3-9b28b4cdc3f7
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 3%

---

# データタイプ：新規および変更済み{#data-types-new-and-modified}

IPS APIバージョン4.5の新しいデータ型と変更されたデータ型について説明します。

構文

## 新しいタイプ {#section-6941b228cf6747a987e98c3d6e4b6b17}

* `AssetSummary`
* `AssetSummaryArray`
* `JobLogDetailAux`
* `JobLogDetailAuxArray`
* `MPEvent`
* `MPEventArray`
* `OperationFault`
* `OperationFaultArray`
* `PhotoshopOptions`
* `TagCondition`
* `TagConditionArray`
* `TagFieldValues`
* `TagFieldValuesArray`
* `TagValueUpdate`
* `TagValueUpdateArray`
* `TagValueUpdateFault`
* `TagValueUpdateFaultArray`
* `UrlArray`

## 変更されたタイプ {#section-6ecdf752cc1a4636a583b4c546a0fccf}

* アセットには、仮想ファイル名を返す新しい`fileName`フィールドが含まれています。
* `AssetSummary` フィールド `type` とフィールドを `name` 返す

* `MetadataField` 内容 `isHidden`

* `MetadataUpdate`
* `UploadUrlsJob` にはが必要で、 `urlArray` オプションのカウントを追加 `numUrls` します
