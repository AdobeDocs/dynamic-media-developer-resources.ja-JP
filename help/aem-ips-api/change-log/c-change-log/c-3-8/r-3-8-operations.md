---
description: IPS APIバージョン3.8の新しい操作方法と変更された操作方法について説明します。
solution: Experience Manager
title: 新規および変更された操作
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '67'
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

