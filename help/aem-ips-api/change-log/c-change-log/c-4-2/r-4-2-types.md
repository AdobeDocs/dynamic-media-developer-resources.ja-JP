---
description: IPS APIバージョン4.2の新しいデータ型と変更されたデータ型について説明します。
solution: Experience Manager
title: 新規および変更されたデータタイプ
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 3%

---


# データタイプ：新規および変更済み{#data-types-new-and-modified}

IPS APIバージョン4.2の新しいデータ型と変更されたデータ型について説明します。

構文

## 新しいタイプ{#section-770a814386a44478881feeff2b6f65f5}

* `AudioInfo`
* `CuePointInfo`
* `PdfSettings`
* `PremeierExpressRemixInfo`

## 変更されたタイプ{#section-6c42b62dd91c4e9bb3a067b9abe3adee}

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

