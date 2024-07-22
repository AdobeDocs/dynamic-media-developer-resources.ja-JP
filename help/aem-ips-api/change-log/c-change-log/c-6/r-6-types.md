---
description: IPS API バージョン 6 の新しいタイプと変更されたタイプについて説明します。
solution: Experience Manager
title: 新規および変更済みのデータタイプ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d3bcd718-cf27-4d31-850f-a3205564be60
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 1%

---

# データタイプ：新規および変更済み{#data-types-new-and-modified}

IPS API バージョン 6 の新しいタイプと変更されたタイプについて説明します。

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

**追加**

* `numUrls` を `UploadUrlsJob` に追加しました。

* が `fileName` を `Asset.` に追加しました

* `isHidden` を `MetadataField` に追加しました。

* `taskState` を `TaskProgress` に追加しました。

* `ActiveJob` と `ScheduledJob` に `exportJob` を追加しました。

* `optmizedPath` と `optimizedFile` を `PsdInfo` に追加しました。

* `contextHandle` が次に追加されました：

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* `Asset` に次のパラメーターを追加しました。

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**変更**

* `User` で、が `role` を `defaultRole` に変更しました。

* `Folder` で、が `permissions` を `permissionsSetHandle` に変更しました。

* `AssetSummary` では、`type` と `name` がオプションになりました。
