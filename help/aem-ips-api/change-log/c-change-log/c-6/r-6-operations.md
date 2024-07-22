---
description: IPS API バージョン 6 の新しい操作メソッドと変更された操作メソッドについて説明します。
solution: Experience Manager
title: 新規および変更済みの操作
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fc7af77e-17fc-453a-8949-78c9c5c33b34
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 1%

---

# 操作：新規および変更{#operations-new-and-modified}

IPS API バージョン 6 の新しい操作メソッドと変更された操作メソッドについて説明します。

構文

## 新しい操作 {#section-088502a0746945f28a5ea100cd655bc6}

* `batchGetAssetPublishContexts`
* `getPublishContexts`
* `moveFolder`
* `setAssetsContexState`
* `updateAssetSet`
* `updateImageSet`

## 変更された操作 {#section-f4e8755527444266ae806e3f4c851ae6}

**追加**

* `isHidden` と `initialTagValue` が次に追加されました：

   * `saveMetadataField`
   * ` `updateMetadataField」
   * `createMetadataField`

* `thumbAssetHandle` が次に追加されました：

   * `createImageSet`
   * `createAssetSet`

  `companyHandle` が次に追加されました：

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`

  `contextHandle` が次に追加されました：

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`

* includeInactive が次に追加されました。

   * `getUsers` をクリックします。
   * `getUserChars` をクリックします。

* `permissionArray` を `createPropertySet` に追加しました。

* `exportJob` を `submitJob` に追加しました。

**変更**

* `addUser` と `setUser` で、`role` を `defaultRole` に変更しました。

* `getCompanyMembers` で、が `userArray` を `memberArray` に変更しました。

* `getCompanyMembership` で、が `companyArray` を `membershipArray` に変更しました。

* `addUser`、`setCompanyMembership` および `addCompanyMembership` では、が `membershipArray` から `companyHandleArray` に変更されました。

* `getCompanyMembership` で、が `companyArray` を `membershipArray` に変更しました。

* `getUserChars` では、`includeInvalid` はオプションになりました。

**削除済み**

* `renameFiles` を `renameAsset` から削除しました。

* `getXMPPanelViewDefinition` を削除しました。
* `searchAssetsByFulltext` と `searchAssetsBySimilarity` を削除しました。
