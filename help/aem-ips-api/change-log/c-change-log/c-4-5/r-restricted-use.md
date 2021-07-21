---
description: ベータ版のWSDLで使用できるこれらの新しい操作や変更された操作およびデータ型は、Dynamic Mediaが開発したアプリケーション以外では使用できません。
solution: Experience Manager
title: 使用制限
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 6602c5bc-9f75-4885-ae14-cab14e6afa5e
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# 使用制限{#restricted-use}

ベータ版のWSDLで使用できるこれらの新しい操作や変更された操作およびデータ型は、Dynamic Mediaが開発したアプリケーション以外では使用できません。

これらの操作およびタイプは、以降のシステム更新で無効化、変更、または廃止される可能性があります。

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

* `ActiveJob`を変更して`createVideoSitemapJob`型を含めるようにしました。

* `ScheduledJob`を変更して`createVideoSitemapJob`型を含めるようにしました。

* `ImageServingPublishJob`を変更し、オプションの`contextHandle`を含めました。

* `ImageRenderingPublishJob`を変更し、オプションの`contextHandle`を含めました。

* `MetadataField`を変更し、オプションの`initialTagField`を含めました。

* `MetadataCondition`を追加し、オプションの`caseSensitive`パラメーターを追加しました。

* `PropertySet`を変更し、オプションの`PermissionArray`を`permissions`に含めるようにしました。

* `UploadDirectoryJob`を変更し、オプションの`xmpKeywords`、`xmpTemplateId`および`xmpTemplateOverride`パラメーターを含めるようにしました。

* `VideoPublishJob`を変更し、オプションの`contextHandle`を含めました。

**変更された操作**

* `createAssetSet`を変更し、オプションの`thumbAssetHandle`を含めました。

* `createImageSet`を変更し、オプションの`thumbAssetHandle`を含めました。

* `createMetadataField`を変更し、オプションの`initialTagValue`パラメーターを含めるようにしました。

* `createPropertySet`を変更し、オプションの`PermissionUpdateArray`を`permissionArray`に含めるようにしました。

* `getImageServingPublishSettings`を変更し、オプションの`contextHandle`パラメーターを含めるようにしました。

* `getImageRenderingPublishSettings`を変更し、オプションの`contextHandle`パラメーターを含めるようにしました。

* `searchAssetsByFullText`を変更し、一連のオプションパラメーターを含めるようにしました。

   * `SearchFilter` パラメータ `filters` ーとして

   * `sortBy`
   * `sortDirection`

* `searchAssetsByMetadata`を変更し、一連のオプションパラメーターを含めるようにしました。

   * `SearchFilter` パラメータ `filters` ーとして

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` 7つのパラメータのシーケンス

* `setAssetPublishState`を変更し、オプションの`HandleArray`を`contextHandleArray`に含めるようにしました。

* `setImageServingPublishSettings`を変更し、オプションの`contextHandle`パラメーターを含めるようにしました。

* `setImageRenderingPublishSettings`を変更し、オプションの`contextHandle`パラメーターを含めるようにしました。

* `submitJob`を変更し、オプションの`createVideoSitemap`ジョブタイプを含めるようにしました。
