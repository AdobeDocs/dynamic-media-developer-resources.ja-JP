---
description: IPS API バージョン 4.2 の新しいデータ型と変更されたデータ型について説明します。
solution: Experience Manager
title: 新規および変更済みのデータタイプ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 3917e778-bd28-4047-b9f8-3063f136e492
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 1%

---

# データタイプ：新規および変更済み{#data-types-new-and-modified}

IPS API バージョン 4.2 の新しいデータ型と変更されたデータ型について説明します。

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
