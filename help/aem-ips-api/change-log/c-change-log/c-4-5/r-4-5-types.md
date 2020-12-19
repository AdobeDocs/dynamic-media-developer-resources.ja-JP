---
description: IPS APIバージョン4.5の新しいデータ型と変更されたデータ型について説明します。
seo-description: IPS APIバージョン4.5の新しいデータ型と変更されたデータ型について説明します。
seo-title: 新規および変更されたデータタイプ
solution: Experience Manager
title: 新規および変更されたデータタイプ
topic: Scene7 Image Production System API
uuid: 2752f9dd-ec47-45d6-a465-6d275ec2b2fb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 2%

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

