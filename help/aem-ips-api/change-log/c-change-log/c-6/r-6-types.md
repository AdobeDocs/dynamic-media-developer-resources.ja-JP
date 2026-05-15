---
description: IPS API バージョン 6の新しいタイプと変更されたタイプについて説明します。
solution: Experience Manager
title: 新規および変更されたデータタイプ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d3bcd718-cf27-4d31-850f-a3205564be60
TQID: 'https://experienceleague.adobe.com/LI8xzlS2eACzYqcV3krzThLm77-z6imYLohPRCTHIYs'
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
source-wordcount: 71
ht-degree: 1%

---

# データタイプ：新規および変更{#data-types-new-and-modified}

IPS API バージョン 6の新しいタイプと変更されたタイプについて説明します。

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

* `numUrls`を`UploadUrlsJob`に追加しました。

* `fileName`を`Asset.`に追加しました

* `isHidden`を`MetadataField`に追加しました。

* `taskState`を`TaskProgress`に追加しました。

* `exportJob`を`ActiveJob`と`ScheduledJob`に追加しました。

* `optmizedPath`と`optimizedFile`を`PsdInfo`に追加しました。

* に`contextHandle`を追加しました：

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* 次のパラメーターを`Asset`に追加しました：

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**変更**

* `User`で、`role`を`defaultRole`に変更しました。

* `Folder`で、`permissions`を`permissionsSetHandle`に変更しました。

* `AssetSummary`では、`type`と`name`はオプションになりました。
