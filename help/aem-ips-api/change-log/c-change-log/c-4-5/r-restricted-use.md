---
description: ベータ版WSDLで使用できる新しい操作や変更された操作およびデータ型は、Scene7が開発したアプリケーション以外では使用できません。
seo-description: ベータ版WSDLで使用できる新しい操作や変更された操作およびデータ型は、Scene7が開発したアプリケーション以外では使用できません。
seo-title: 使用制限
solution: Experience Manager
title: 使用制限
topic: Scene7 Image Production System API
uuid: 76a423e5-ff7d-44a3-aba4-af258ea55256
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---


# 制限付き使用{#restricted-use}

ベータ版WSDLで使用できる新しい操作や変更された操作およびデータ型は、Scene7が開発したアプリケーション以外では使用できません。

これらの操作とタイプは、以降のシステム更新で無効化、変更、または非推奨になる場合があります。

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
* searchAssetsBySimporibility
* searchAssetsByFulltext
* setAssetPublishState
* setPropertySetPermissions
* updateAssetSet
* updateCompanyMetadata
* updateImageSet
* updatePropertySetPermissions

**変更されたタイプ**

* `ActiveJob`を`createVideoSitemapJob`型を含めるように変更しました

* `ScheduledJob`を`createVideoSitemapJob`型を含めるように変更しました

* `ImageServingPublishJob`を変更し、オプションの`contextHandle`を含めました

* `ImageRenderingPublishJob`を変更し、オプションの`contextHandle`を含めました

* `MetadataField`を変更し、オプションの`initialTagField`を含めました

* `MetadataCondition`を、オプションの`caseSensitive`パラメーターを含めるように変更しました

* `PropertySet`を`permissions`に変更し、オプションの`PermissionArray`を含めました。

* オプションの`xmpKeywords`、`xmpTemplateId`、`xmpTemplateOverride`パラメーターを含めるように`UploadDirectoryJob`を変更しました

* `VideoPublishJob`を変更し、オプションの`contextHandle`を含めました

**変更された操作**

* `createAssetSet`を変更し、オプションの`thumbAssetHandle`を含めました

* `createImageSet`を変更し、オプションの`thumbAssetHandle`を含めました

* オプションの`initialTagValue`パラメーターを含めるように`createMetadataField`を変更しました

* `createPropertySet`を`permissionArray`に変更し、オプションの`PermissionUpdateArray`を含めました。

* オプションの`contextHandle`パラメーターを含めるように`getImageServingPublishSettings`を変更しました

* オプションの`contextHandle`パラメーターを含めるように`getImageRenderingPublishSettings`を変更しました

* `searchAssetsByFullText`を変更し、一連のオプションのパラメーターを含めるようにしました。

   * `SearchFilter` パラメー `filters` ターとして

   * `sortBy`
   * `sortDirection`

* `searchAssetsByMetadata`を変更し、一連のオプションのパラメーターを含めるようにしました。

   * `SearchFilter` パラメー `filters` ターとして

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` 7つのパラメーターのシーケンス

* `setAssetPublishState`を`contextHandleArray`に変更し、オプションの`HandleArray`を含めました。

* オプションの`contextHandle`パラメーターを含めるように`setImageServingPublishSettings`を変更しました

* `setImageRenderingPublishSettings`を変更し、オプションの`contextHandle`パラメーターを含めるようにしました

* オプションの`createVideoSitemap`ジョブの種類を含めるように`submitJob`を変更しました

