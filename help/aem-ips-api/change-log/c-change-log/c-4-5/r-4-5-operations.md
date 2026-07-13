---
description: IPS API バージョン 4.5の新しい運用方法と変更された運用方法について説明します。
solution: Experience Manager
title: 操作 – 新規および変更
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9033328a-d0ce-4ef2-b6ec-c6a81fbedf9d
TQID: 'https://experienceleague.adobe.com/n4U8LW8otIaBBDalW1wRJFaweTAw3-0Sh0ckgIEADAI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 1%

---

# 操作：新規および変更{#operations-new-and-modified}

IPS API バージョン 4.5の新しい運用方法と変更された運用方法について説明します。

構文

## 新しいオペレーション {#section-a3be679d8e9345aba2e97699c3a537b9}

* `addMediaPortalEvent`
* `addTagFieldValues`
* `cdnCacheInvalidation`
* `deleteTagFieldValues`
* `deleteTagFieldValues`
* `getDistinctMetadataValues`
* `getMediaPortalEvent`
* `getTagFieldValues`
* `getXMPPacket`
* `searchAssetsByFullText`
* `searchAssetsByMetadata`
* `setTagFieldValues`
* `updateTagFieldValues`
* `updateXMPPacket`

## 修正された操作 {#section-1c022cc62d274c349837013f1c02ca51}

* `Asset`には、`animatedGifInfo`、`swcInfo`、`cssInfo`および`javascriptInfo`個のパラメーターが含まれています。
* `createMetadataField`には、オプションの`isHidden` パラメーターが含まれています。
* `saveMetadataField`には、オプションの`isHidden` パラメーターが含まれています。
* `searchAssets`
* 以前のリリースでは、`renameFiles` パラメーターは廃止され、`renameAsset`操作から削除されました。 仮想ファイルパスは、新しいアセット名に一致するように変更されますが（ファイル拡張子は保持されます）、物理ファイルパスは影響を受けません。 API クライアントは、新しいAPI バージョンに更新する際に、このパラメーターへの参照を削除する必要があります。

