---
description: IPS APIバージョン4.5の新しいデータタイプと変更されたデータタイプについて説明します。
seo-description: IPS APIバージョン4.5の新しいデータタイプと変更されたデータタイプについて説明します。
seo-title: 新規および変更されたデータタイプ
solution: Experience Manager
title: 新規および変更されたデータタイプ
topic: Scene7 Image Production System API
uuid: 2752f9dd-ec47-45d6-a465-6d275ec2b2fb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# データタイプ：新規および変更済み{#data-types-new-and-modified}

IPS APIバージョン4.5の新しいデータタイプと変更されたデータタイプについて説明します。

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

* アセットに、仮想ファイ `fileName` ル名を返す新しいフィールドが含まれています。
* `AssetSummary` フィールド `type` とを返 `name` す

* `MetadataField` 内容 `isHidden`

* `MetadataUpdate`
* `UploadUrlsJob` には必ず値を `urlArray` 追加し、オプションの数を追加し `numUrls` ます

