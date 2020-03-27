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

---


# データタイプ：新規および変更済み{#data-types-new-and-modified}

IPS APIバージョン6の新しいタイプと変更されたタイプについて説明します。

構文

## 新しいタイプ {#section-71ba6954339e4ba899acdf8a3212d6f3}

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

## 変更されたタイプ {#section-56b834b1a3b843279d8715b4a4f3890b}

**追加済み**

* に追加さ `numUrls` れまし `UploadUrlsJob`た。

* 追加 `fileName` 先 `Asset.`

* に追加さ `isHidden` れまし `MetadataField`た。

* に追加さ `taskState` れまし `TaskProgress`た。

* とに追 `exportJob` 加さ `ActiveJob` れまし `ScheduledJob`た。

* とがに追 `optmizedPath` 加さ `optimizedFile` れまし `PsdInfo`た。

* 次に追 `contextHandle` 加：

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* 次のパラメーターをに追加しまし `Asset`た。

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**変更**

* で、 `User`に変更 `role` しまし `defaultRole`た。

* で、 `Folder`に変更 `permissions` しまし `permissionsSetHandle`た。

* で、およ `AssetSummary`びはオ `type` プショ `name` ンになりました。

