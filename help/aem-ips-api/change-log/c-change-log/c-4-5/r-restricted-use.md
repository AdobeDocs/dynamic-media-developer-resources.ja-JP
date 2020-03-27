---
description: ベータ版WSDLで使用できる新しい操作や変更された操作やデータ型は、Scene7が開発したアプリケーションの外部では使用できません。
seo-description: ベータ版WSDLで使用できる新しい操作や変更された操作やデータ型は、Scene7が開発したアプリケーションの外部では使用できません。
seo-title: 使用制限
solution: Experience Manager
title: 使用制限
topic: Scene7 Image Production System API
uuid: 76a423e5-ff7d-44a3-aba4-af258ea55256
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 使用制限{#restricted-use}

ベータ版WSDLで使用できる新しい操作や変更された操作やデータ型は、Scene7が開発したアプリケーションの外部では使用できません。

これらの操作とタイプは、以降のシステム更新で無効化、変更、または廃止される可能性があります。

**新しいタイプ**

* AssetPublishContexts
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

**変更されたタイプ**

* タイプを `ActiveJob` 含めるように変更され `createVideoSitemapJob` ました

* タイプを `ScheduledJob` 含めるように変更され `createVideoSitemapJob` ました

* オプション `ImageServingPublishJob` の `contextHandle`

* オプション `ImageRenderingPublishJob` の `contextHandle`

* オプション `MetadataField` の `initialTagField`

* 含めるパラメ `MetadataCondition` ーターとオプションのパラメーターに変 `caseSensitive` 更

* オプシ `PropertySet``PermissionArray` ョンの `permissions`

* オプション `UploadDirectoryJob` およびパラメーターを含め `xmpKeywords`るように `xmpTemplateId` 変更されま `xmpTemplateOverride` した

* オプション `VideoPublishJob` の `contextHandle`

**変更された操作**

* オプション `createAssetSet` の `thumbAssetHandle`

* オプション `createImageSet` の `thumbAssetHandle`

* オプション `createMetadataField` のパラメーターを含めるように変更され `initialTagValue` ました

* オプシ `createPropertySet``PermissionUpdateArray` ョンの `permissionArray`

* オプション `getImageServingPublishSettings` のパラメーターを含めるように変更され `contextHandle` ました

* オプション `getImageRenderingPublishSettings` のパラメーターを含めるように変更され `contextHandle` ました

* 一連のオ `searchAssetsByFullText` プションのパラメーターを含めるように変更されました。

   * `SearchFilter` パラメータ `filters` ー

   * `sortBy`
   * `sortDirection`

* 一連のオ `searchAssetsByMetadata` プションのパラメーターを含めるように変更されました。

   * `SearchFilter` パラメータ `filters` ー

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` 7つのパラメータのシーケンス

* オプシ `setAssetPublishState``HandleArray` ョンの `contextHandleArray`

* オプション `setImageServingPublishSettings` のパラメーターを含めるように変更され `contextHandle` ました

* オプション `setImageRenderingPublishSettings` のパラメーターを含めるように変更され `contextHandle`ました

* オプション `submitJob` のジョブタイプを含めるように変 `createVideoSitemap` 更されました

