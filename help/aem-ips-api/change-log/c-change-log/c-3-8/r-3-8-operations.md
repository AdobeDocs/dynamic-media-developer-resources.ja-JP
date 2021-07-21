---
description: IPS APIバージョン3.8の新しい操作方法と変更された操作方法について説明します。
solution: Experience Manager
title: 新規および変更された操作
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 8f4fe698-afe8-4ce6-904d-42fa67dee4dd
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 1%

---

# 操作：新規および変更済み{#operations-new-and-modified}

IPS APIバージョン3.8の新しい操作方法と変更された操作方法について説明します。

構文

## 新しい操作 {#section-64f0e4cd01154bb68c4e3e2dd8732ef5}

* `setAssetPublishState`
* `saveZoomTarget`
* `deleteZoomTarget`
* `saveImageMap`
* `deleteImageMap`
* `createImageSet`
* `getImageSetMembers`

## 変更された操作 {#section-25eee732b69c49d0a27b1f3290f8654a}

**searchAssets**

* オプションの`publishState`パラメーターを使用すると、アセットの状態を`MarkedForPublish/NotMarkedForPublish`で検索できます。

**getJobLogs**

* オプションの`userHandle`パラメーターを使用すると、特定のユーザーから送信されたジョブのログを取得できます。
