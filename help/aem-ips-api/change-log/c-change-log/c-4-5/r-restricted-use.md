---
description: ベータ版 WSDL で使用できるこれらの新しいまたは変更された操作とデータタイプは、Dynamic Media で開発されたアプリケーション以外では使用できません。
solution: Experience Manager
title: 使用制限
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6602c5bc-9f75-4885-ae14-cab14e6afa5e
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# 使用制限{#restricted-use}

ベータ版 WSDL で使用できるこれらの新しいまたは変更された操作とデータタイプは、Dynamic Media で開発されたアプリケーション以外では使用できません。

これらの操作やタイプは、その後のシステム更新で、無効化、変更または非推奨（廃止予定）になる場合があります。

**新しいタイプ**

* AssetPublishContext
* AssetPublishContextsArray
* CompanyMetadataInfo
* CompanyMetadataInfoArray
* CreateVideoSitemapJob
* PublishContext
* PublishContextArray
* SearchFilter
* LongArray

**新しい操作**

* applyMetadataTemplate
* batchGetAssetPublishContexts
* createCompanyMetadata
* deleteCompanyMetadata
* getCompanyMetadata
* getPublishContexts
* listCompanyMetadata
* removeMask
* removePropertySetPermissions
* searchAssetsBySimilarity
* searchAssetsByFulltext
* setAssetPublishState
* setPropertySetPermissions
* updateAssetSet
* updateCompanyMetadata
* updateImageSet
* updatePropertySetPermissions

**変更された型**

* `ActiveJob` が `createVideoSitemapJob` タイプを含むように変更されました

* `ScheduledJob` が `createVideoSitemapJob` タイプを含むように変更されました

* オプションの `ImageServingPublishJob` を含むように `contextHandle` を変更しました

* オプションの `ImageRenderingPublishJob` を含むように `contextHandle` を変更しました

* オプションの `MetadataField` を含むように `initialTagField` を変更しました

* `MetadataCondition` が追加され、オプションの `caseSensitive` パラメーターが追加されました

* `PropertySet` が `PermissionArray` としてオプションの `permissions` を含むように変更されました

* オプションの `UploadDirectoryJob`、`xmpKeywords`、`xmpTemplateId` パラメーターを含むように `xmpTemplateOverride` を変更しました

* オプションの `VideoPublishJob` を含むように `contextHandle` を変更しました

**変更された操作**

* オプションの `createAssetSet` を含むように `thumbAssetHandle` を変更しました

* オプションの `createImageSet` を含むように `thumbAssetHandle` を変更しました

* オプションの `createMetadataField` パラメーターを含むように `initialTagValue` を変更しました

* `createPropertySet` が `PermissionUpdateArray` としてオプションの `permissionArray` を含むように変更されました

* オプションの `getImageServingPublishSettings` パラメーターを含むように `contextHandle` を変更しました

* オプションの `getImageRenderingPublishSettings` パラメーターを含むように `contextHandle` を変更しました

* 一連のオプションパラメーターを含むように `searchAssetsByFullText` を変更しました。

   * `SearchFilter` as `filters` パラメーター

   * `sortBy`
   * `sortDirection`

* 一連のオプションパラメーターを含むように `searchAssetsByMetadata` を変更しました。

   * `SearchFilter` as `filters` パラメーター

   * `sortBy`
   * `sortDirection`
   * 7 つのパラメ `haystackSearch` ターのシーケンス

* `setAssetPublishState` が `HandleArray` としてオプションの `contextHandleArray` を含むように変更されました

* オプションの `setImageServingPublishSettings` パラメーターを含むように `contextHandle` を変更しました

* オプションの `setImageRenderingPublishSettings` パラメーターを含むように `contextHandle` を変更しました

* オプションの `submitJob` ジョブタイプを含むように `createVideoSitemap` を変更しました
