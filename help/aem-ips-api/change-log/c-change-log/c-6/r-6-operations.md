---
description: IPS API バージョン 6の新しい運用方法と変更された運用方法について説明します。
solution: Experience Manager
title: 新規および変更された操作
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fc7af77e-17fc-453a-8949-78c9c5c33b34
TQID: 'https://experienceleague.adobe.com/DLA26IsxxpZ0TSSfQBrvZSl8mbcJCaTfnpK-bhhmglg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 85
ht-degree: 3%

---

# 操作：新規および変更{#operations-new-and-modified}

IPS API バージョン 6の新しい運用方法と変更された運用方法について説明します。

構文

## 新しいオペレーション {#section-088502a0746945f28a5ea100cd655bc6}

* `batchGetAssetPublishContexts`
* `getPublishContexts`
* `moveFolder`
* `setAssetsContexState`
* `updateAssetSet`
* `updateImageSet`

## 修正された操作 {#section-f4e8755527444266ae806e3f4c851ae6}

**追加**

* `isHidden`と`initialTagValue`を次の場所に追加しました：

   * `saveMetadataField`
   * ` `updateMetadataField&quot;
   * `createMetadataField`

* に`thumbAssetHandle`を追加しました：

   * `createImageSet`
   * `createAssetSet`

  に`companyHandle`を追加しました：

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`

  に`contextHandle`を追加しました：

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`

* includeInactiveを次の場所に追加しました：

   * `getUsers`.
   * `getUserChars`.

* `permissionArray`を`createPropertySet`に追加しました。

* `exportJob`を`submitJob`に追加しました。

**変更**

* `addUser`と`setUser`で、`role`を`defaultRole`に変更しました。

* `getCompanyMembers`で、`userArray`を`memberArray`に変更しました。

* `getCompanyMembership`で、`companyArray`を`membershipArray`に変更しました。

* `addUser`、`setCompanyMembership`、`addCompanyMembership`では、`membershipArray`が`companyHandleArray`に変更されました。

* `getCompanyMembership`で、`companyArray`を`membershipArray`に変更しました。

* `getUserChars`では、`includeInvalid`はオプションになりました。

**削除済み**

* `renameFiles`を`renameAsset`から削除しました。

* `getXMPPanelViewDefinition`を削除しました。
* `searchAssetsByFulltext`と`searchAssetsBySimilarity`を削除しました。

