---
description: IPS APIバージョン4.5の新しいデータ型と変更されたデータ型について説明します。
solution: Experience Manager
title: 新規および変更されたデータタイプ
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 3%

---


# データタイプ：新規および変更済み{#data-types-new-and-modified}

IPS APIバージョン4.5の新しいデータ型と変更されたデータ型について説明します。

構文

## 新しいタイプ{#section-6941b228cf6747a987e98c3d6e4b6b17}

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

## 変更されたタイプ{#section-6ecdf752cc1a4636a583b4c546a0fccf}

* アセットには、仮想ファイル名を返す新しい`fileName`フィールドが含まれています。
* `AssetSummary` 戻り値 `type` と `name` フィールド

* `MetadataField` 内容 `isHidden`

* `MetadataUpdate`
* `UploadUrlsJob` には `urlArray` が必要で、オプションの `numUrls` 数を追加します。

