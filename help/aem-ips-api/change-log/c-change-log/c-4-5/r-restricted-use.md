---
description: ベータ版 WSDL で使用できるこれらの新しいまたは変更された操作とデータタイプは、Dynamic Mediaで開発されたアプリケーション以外では使用できません。
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

ベータ版 WSDL で使用できるこれらの新しいまたは変更された操作とデータタイプは、Dynamic Mediaで開発されたアプリケーション以外では使用できません。

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

* オプションの `contextHandle` を含むように `ImageServingPublishJob` を変更しました

* オプションの `contextHandle` を含むように `ImageRenderingPublishJob` を変更しました

* オプションの `initialTagField` を含むように `MetadataField` を変更しました

* `MetadataCondition` が追加され、オプションの `caseSensitive` パラメーターが追加されました

* `PropertySet` が `permissions` としてオプションの `PermissionArray` を含むように変更されました

* オプションの `xmpKeywords`、`xmpTemplateId`、`xmpTemplateOverride` パラメーターを含むように `UploadDirectoryJob` を変更しました

* オプションの `contextHandle` を含むように `VideoPublishJob` を変更しました

**変更された操作**

* オプションの `thumbAssetHandle` を含むように `createAssetSet` を変更しました

* オプションの `thumbAssetHandle` を含むように `createImageSet` を変更しました

* オプションの `initialTagValue` パラメーターを含むように `createMetadataField` を変更しました

* `createPropertySet` が `permissionArray` としてオプションの `PermissionUpdateArray` を含むように変更されました

* オプションの `contextHandle` パラメーターを含むように `getImageServingPublishSettings` を変更しました

* オプションの `contextHandle` パラメーターを含むように `getImageRenderingPublishSettings` を変更しました

* 一連のオプションパラメーターを含むように `searchAssetsByFullText` を変更しました。

   * `SearchFilter` as `filters` パラメーター

   * `sortBy`
   * `sortDirection`

* 一連のオプションパラメーターを含むように `searchAssetsByMetadata` を変更しました。

   * `SearchFilter` as `filters` パラメーター

   * `sortBy`
   * `sortDirection`
   * 7 つのパラメ `haystackSearch` ターのシーケンス

* `setAssetPublishState` が `contextHandleArray` としてオプションの `HandleArray` を含むように変更されました

* オプションの `contextHandle` パラメーターを含むように `setImageServingPublishSettings` を変更しました

* オプションの `contextHandle` パラメーターを含むように `setImageRenderingPublishSettings` を変更しました

* オプションの `createVideoSitemap` ジョブタイプを含むように `submitJob` を変更しました
