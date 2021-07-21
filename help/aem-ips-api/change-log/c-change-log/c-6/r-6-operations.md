---
description: IPS APIバージョン6の新しい操作方法と変更された操作方法について説明します。
solution: Experience Manager
title: 新規および変更された操作
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: fc7af77e-17fc-453a-8949-78c9c5c33b34
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 1%

---

# 操作：新規および変更済み{#operations-new-and-modified}

IPS APIバージョン6の新しい操作方法と変更された操作方法について説明します。

構文

## 新しい操作 {#section-088502a0746945f28a5ea100cd655bc6}

* `batchGetAssetPublishContexts`
* `getPublishContexts`
* `moveFolder`
* `setAssetsContexState`
* `updateAssetSet`
* `updateImageSet`

## 変更された操作 {#section-f4e8755527444266ae806e3f4c851ae6}

**追加済み**

* `isHidden`と`initialTagValue`を次の場所に追加しました。

   * `saveMetadataField`
   * ` `updateMetadataField&quot;
   * `createMetadataField`

* `thumbAssetHandle`を次の場所に追加しました。

   * `createImageSet`
   * `createAssetSet`

   `companyHandle`を次の場所に追加しました。

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`

   `contextHandle`を次の場所に追加しました。

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`



* includeInactiveを次の場所に追加しました。

   * `getUsers` をクリックします。
   * `getUserChars` をクリックします。

* `permissionArray`を`createPropertySet`に追加しました。

* `exportJob`を`submitJob`に追加しました。

**変更済み**

* `addUser`と`setUser`で、`role`を`defaultRole`に変更しました。

* `getCompanyMembers`で、`userArray`を`memberArray`に変更しました。

* `getCompanyMembership`で、`companyArray`を`membershipArray`に変更しました。

* `addUser`、`setCompanyMembership`、および`addCompanyMembership`で、`membershipArray`を`companyHandleArray`に変更しました。

* `getCompanyMembership`で、`companyArray`を`membershipArray`に変更しました。

* `getUserChars`では、`includeInvalid`はオプションになりました。

**削除**

* `renameAsset`から`renameFiles`を削除しました。

* `getXMPPanelViewDefinition`を削除しました。
* `searchAssetsByFulltext`と`searchAssetsBySimilarity`を削除しました。
