---
description: IPS APIバージョン3.8の新しい操作方法と変更された操作方法について説明します。
seo-description: IPS APIバージョン3.8の新しい操作方法と変更された操作方法について説明します。
seo-title: 新規および変更された操作
solution: Experience Manager
title: 新規および変更された操作
topic: Scene7 Image Production System API
uuid: e836c5af-53b8-4bfa-a93a-98750cca9745
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 1%

---


# 操作：新規および変更済み{#operations-new-and-modified}

IPS APIバージョン3.8の新しい操作方法と変更された操作方法について説明します。

構文

## 新しい操作{#section-64f0e4cd01154bb68c4e3e2dd8732ef5}

* `setAssetPublishState`
* `saveZoomTarget`
* `deleteZoomTarget`
* `saveImageMap`
* `deleteImageMap`
* `createImageSet`
* `getImageSetMembers`

## 変更された操作{#section-25eee732b69c49d0a27b1f3290f8654a}

**searchAssets**

* オプションの`publishState`パラメーターを使用すると、`MarkedForPublish/NotMarkedForPublish`アセット状態を検索できます。

**getJobLogs**

* オプションの`userHandle`パラメーターを使用すると、特定のユーザーによって送信されたジョブログを取得できます。

