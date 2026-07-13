---
description: IPS API バージョン 4.2の新しいデータ型と変更されたデータ型について説明します。
solution: Experience Manager
title: 新規および変更されたデータタイプ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 3917e778-bd28-4047-b9f8-3063f136e492
TQID: 'https://experienceleague.adobe.com/2YCgrii3dF6Zq7NlXRI0vD3DtO-jWpSo4YKcpZsdFHU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 53
ht-degree: 1%

---

# データタイプ：新規および変更{#data-types-new-and-modified}

IPS API バージョン 4.2の新しいデータ型と変更されたデータ型について説明します。

構文

## 新しいタイプ {#section-770a814386a44478881feeff2b6f65f5}

* `AudioInfo`
* `CuePointInfo`
* `PdfSettings`
* `PremeierExpressRemixInfo`

## 変更されたタイプ {#section-6c42b62dd91c4e9bb3a067b9abe3adee}

**アセット**

追加されたパラメーター：

* `readyForPublish`
* `trashState`
* `MaskInfo`
* `RTFInfo`

削除されたパラメーター：

* `ImageSetInfo`
* `RenderSetInfo`

**ReprocessAssetsJob**

追加されたパラメーター：

* `preservePublishState`
* `preserveCrop`
* `readyForPublish`

**UploadDirectoryJob**

追加されたパラメーター：

* `preservePublishState`
* `preserveCrop`
* `videoEncodingPreset`

**UploadUrlsJob**

追加されたパラメーター：

* `preservePublishState`
* `preserveCrop`

