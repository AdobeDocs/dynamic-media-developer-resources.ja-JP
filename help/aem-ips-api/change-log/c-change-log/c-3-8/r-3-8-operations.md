---
description: IPS API バージョン 3.8の新しい運用方法と変更された運用方法について説明します。
solution: Experience Manager
title: 新規および変更された操作
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8f4fe698-afe8-4ce6-904d-42fa67dee4dd
TQID: 'https://experienceleague.adobe.com/ABGdwOL99oGAXt9UBLNVYQrGxAQ3S9nlDDTHRZNt1Xo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 62
ht-degree: 1%

---

# 操作：新規および変更{#operations-new-and-modified}

IPS API バージョン 3.8の新しい運用方法と変更された運用方法について説明します。

構文

## 新しいオペレーション {#section-64f0e4cd01154bb68c4e3e2dd8732ef5}

* `setAssetPublishState`
* `saveZoomTarget`
* `deleteZoomTarget`
* `saveImageMap`
* `deleteImageMap`
* `createImageSet`
* `getImageSetMembers`

## 修正された操作 {#section-25eee732b69c49d0a27b1f3290f8654a}

**searchAssets**

* オプションの`publishState` パラメーターを使用すると、`MarkedForPublish/NotMarkedForPublish` アセットの状態を検索できます。

**getJobLogs**

* オプションの`userHandle` パラメーターを使用すると、特定のユーザーが送信したジョブ ログを取得できます。
