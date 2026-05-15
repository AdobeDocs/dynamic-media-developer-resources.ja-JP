---
description: ベータ版WSDLで利用できる、これらの新しい操作や変更された操作およびデータ型は、Dynamic Mediaが開発したアプリケーション以外では使用できません。
solution: Experience Manager
title: 制限付き使用
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6602c5bc-9f75-4885-ae14-cab14e6afa5e
TQID: 'https://experienceleague.adobe.com/X-Q28iVTM95SDSwlSy3yhmJcfJv0TC3LtxXPRv8RCpg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 232
ht-degree: 0%

---

# 制限付き使用{#restricted-use}

ベータ版WSDLで利用できる、これらの新しい操作や変更された操作およびデータ型は、Dynamic Mediaが開発したアプリケーション以外では使用できません。

これらの操作およびタイプは、その後のシステム更新で無効化、変更、または非推奨になる可能性があります。

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

* `ActiveJob`を`createVideoSitemapJob`型を含むように変更しました

* `ScheduledJob`を`createVideoSitemapJob`型を含むように変更しました

* `ImageServingPublishJob`を変更して、オプションの`contextHandle`を含めました

* `ImageRenderingPublishJob`を変更して、オプションの`contextHandle`を含めました

* `MetadataField`を変更して、オプションの`initialTagField`を含めました

* `MetadataCondition`を含めるように変更し、オプションの`caseSensitive` パラメーターを含めました

* `PropertySet`を変更し、オプションの`PermissionArray`を`permissions`として含めました

* `UploadDirectoryJob`を変更して、オプションの`xmpKeywords`、`xmpTemplateId`、`xmpTemplateOverride`個のパラメーターを含めました

* `VideoPublishJob`を変更して、オプションの`contextHandle`を含めました

**変更された操作**

* `createAssetSet`を変更して、オプションの`thumbAssetHandle`を含めました

* `createImageSet`を変更して、オプションの`thumbAssetHandle`を含めました

* `createMetadataField`を変更して、オプションの`initialTagValue` パラメーターを含めました

* `createPropertySet`を変更し、オプションの`PermissionUpdateArray`を`permissionArray`として含めました

* `getImageServingPublishSettings`を変更して、オプションの`contextHandle` パラメーターを含めました

* `getImageRenderingPublishSettings`を変更して、オプションの`contextHandle` パラメーターを含めました

* `searchAssetsByFullText`を変更して、一連のオプション パラメーターを含めました：

   * `SearchFilter`を`filters` パラメーターとして

   * `sortBy`
   * `sortDirection`

* `searchAssetsByMetadata`を変更して、一連のオプション パラメーターを含めました：

   * `SearchFilter`を`filters` パラメーターとして

   * `sortBy`
   * `sortDirection`
   * 7つのパラメーターの`haystackSearch` シーケンス

* `setAssetPublishState`を変更し、オプションの`HandleArray`を`contextHandleArray`として含めました

* `setImageServingPublishSettings`を変更して、オプションの`contextHandle` パラメーターを含めました

* `setImageRenderingPublishSettings`を変更し、オプションの`contextHandle` パラメーターを含めました

* `submitJob`を変更して、オプションの`createVideoSitemap` ジョブタイプを含めました
