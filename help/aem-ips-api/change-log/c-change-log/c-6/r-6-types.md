---
description: IPS APIバージョン6の新しいタイプと変更されたタイプについて説明します。
seo-description: IPS APIバージョン6の新しいタイプと変更されたタイプについて説明します。
seo-title: 新規および変更されたデータタイプ
solution: Experience Manager
title: 新規および変更されたデータタイプ
topic: Scene7 Image Production System API
uuid: ef7c43ee-467f-46b9-bd82-05e8359bd829
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 1%

---


# データタイプ：新規および変更済み{#data-types-new-and-modified}

IPS APIバージョン6の新しいタイプと変更されたタイプについて説明します。

構文

## 新しいタイプ{#section-71ba6954339e4ba899acdf8a3212d6f3}

* `AssetContextStateUpdate`
* `AssetContextStateUpdateArray`
* `AssetPublishContexts`
* `AssetPublishContextsArray`
* `CompanyMember`
* `CompanyMemberArray`
* `CompanyMembershipUpdate`
* `CompanyMembershipUpdateArray`
* `ContextStateUpdate`
* `ContextStateUpdateArray`
* `Export Job`
* `PermissionsSet`
* `PermissionsSetArray`
* `PublishContext`
* `PublishContextArray`

## 変更されたタイプ{#section-56b834b1a3b843279d8715b4a4f3890b}

**追加済み**

* `numUrls`を`UploadUrlsJob`に追加しました。

* `fileName`を`Asset.`に追加

* `isHidden`を`MetadataField`に追加しました。

* `taskState`を`TaskProgress`に追加しました。

* `exportJob`を`ActiveJob`と`ScheduledJob`に追加しました。

* `optmizedPath`と`optimizedFile`を`PsdInfo`に追加しました。

* `contextHandle`を次に追加：

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* `Asset`に次のパラメーターを追加しました。

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**変更済み**

* `User`で、`role`を`defaultRole`に変更しました。

* `Folder`で、`permissions`を`permissionsSetHandle`に変更しました。

* `AssetSummary`では、`type`と`name`はオプションになりました。

