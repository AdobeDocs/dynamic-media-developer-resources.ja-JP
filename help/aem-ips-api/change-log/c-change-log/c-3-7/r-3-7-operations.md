---
description: IPS APIバージョン3.7の新しい操作方法と変更された操作方法について説明します。
seo-description: IPS APIバージョン3.7の新しい操作方法と変更された操作方法について説明します。
seo-title: 新規および変更された操作
solution: Experience Manager
title: 新規および変更された操作
topic: Scene7 Image Production System API
uuid: 3c163157-cd0d-4887-a1f0-7941d96c36f9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 1%

---


# 操作：新規および変更済み{#operations-new-and-modified}

IPS APIバージョン3.7の新しい操作方法と変更された操作方法について説明します。

構文

## 新しい操作{#section-c4d34a58f8194d548fbe26ab3764ea58}

* `moveAsset`
* `renameAsset`
* `deleteAsset`
* `createFolder`
* `deleteFolder`
* `getActiveJobs`
* `getScheduledJobs`
* `getJobLogs`
* `getJbLogDetails`
* `submitJob`
* `stopJob`
* `pauseJob`
* `resumeJob`
* `executeJob`
* `deleteJob`

## 変更された操作{#section-596ea55a371e4c2ab5531e21ea9d8090}

**searchAsset**

* `name`パラメーターを削除しました。
* `excludeFieldArray`を追加しました。

**getFolders**

* `excludeFieldArray`を追加しました。

**getFolderTree**

* `excludeFieldArray`と`getUniqueMetadataValues`を追加しました。
* `fieldHandle`を必須パラメータにしました。

