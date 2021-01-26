---
description: IPS APIバージョン3.7の新しい操作方法と変更された操作方法について説明します。
solution: Experience Manager
title: 新規および変更された操作
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 2%

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

