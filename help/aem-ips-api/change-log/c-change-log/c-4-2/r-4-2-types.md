---
description: IPS APIバージョン4.2の新しいデータ型と変更されたデータ型について説明します。
solution: Experience Manager
title: 新規および変更されたデータタイプ
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '51'
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

