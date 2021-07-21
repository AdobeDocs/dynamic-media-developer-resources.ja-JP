---
description: IPS APIバージョン3.7の新しい操作方法と変更された操作方法について説明します。
solution: Experience Manager
title: 新規および変更された操作
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 1f11a686-7239-4922-a608-5330864184ac
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 1%

---

# 操作：新規および変更済み{#operations-new-and-modified}

IPS APIバージョン3.7の新しい操作方法と変更された操作方法について説明します。

構文

## 新しい操作 {#section-c4d34a58f8194d548fbe26ab3764ea58}

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

## 変更された操作 {#section-596ea55a371e4c2ab5531e21ea9d8090}

**searchAsset**

* `name`パラメーターを削除しました。
* `excludeFieldArray`を追加しました。

**getFolders**

* `excludeFieldArray`を追加しました。

**getFolderTree**

* `excludeFieldArray`と`getUniqueMetadataValues`を追加しました。
* `fieldHandle`を必須のパラメータにしました。
