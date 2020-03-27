---
description: IPS APIバージョン6の新しい操作方法と変更された操作方法について説明します。
seo-description: IPS APIバージョン6の新しい操作方法と変更された操作方法について説明します。
seo-title: 新規および変更された操作
solution: Experience Manager
title: 新規および変更された操作
topic: Scene7 Image Production System API
uuid: e36f0d5c-0170-4a65-9347-c7fd3538726b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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

* 追加 `isHidden` 先と追 `initialTagValue` 加先：

   * `saveMetadataField`
   * ` `updateMetadataField&quot;
   * `createMetadataField`

* 次に追 `thumbAssetHandle` 加：

   * `createImageSet`
   * `createAssetSet`
   次に追 `companyHandle` 加：

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`
   次に追 `contextHandle` 加：

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`



* includeInactiveが次の場所に追加されました。

   * `getUsers` をクリックします。
   * `getUserChars` をクリックします。

* に追加さ `permissionArray` れまし `createPropertySet`た。

* に追加さ `exportJob` れまし `submitJob`た。

**変更**

* とで、 `addUser` に変 `setUser`更しま `role` した `defaultRole`。

* で、 `getCompanyMembers`に変更 `userArray` しまし `memberArray`た。

* で、 `getCompanyMembership`に変更 `companyArray` しまし `membershipArray`た。

* で、お `addUser`よび `setCompanyMembership`がに変 `addCompanyMembership`更され `membershipArray` まし `companyHandleArray`た。

* で、 `getCompanyMembership`に変更 `companyArray` しまし `membershipArray`た。

* では、がオ `getUserChars`プショ `includeInvalid` ンになりました。

**削除**

* から削 `renameFiles` 除されま `renameAsset`した。

* Removed `getXMPPanelViewDefinition`.
* とを削 `searchAssetsByFulltext` 除しま `searchAssetsBySimilarity`した。

