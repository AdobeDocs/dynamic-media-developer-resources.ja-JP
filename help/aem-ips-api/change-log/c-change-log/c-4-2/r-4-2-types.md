---
description: IPS APIバージョン4.2の新しいデータタイプと変更されたデータタイプについて説明します。
seo-description: IPS APIバージョン4.2の新しいデータタイプと変更されたデータタイプについて説明します。
seo-title: 新規および変更されたデータタイプ
solution: Experience Manager
title: 新規および変更されたデータタイプ
topic: Scene7 Image Production System API
uuid: 274e49da-9eb8-4082-971c-056acb47a53e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# データタイプ：新規および変更済み{#data-types-new-and-modified}

IPS APIバージョン4.2の新しいデータタイプと変更されたデータタイプについて説明します。

構文

## 新しいタイプ {#section-770a814386a44478881feeff2b6f65f5}

* `AudioInfo`
* `CuePointInfo`
* `PdfSettings`
* `PremeierExpressRemixInfo`

## 変更されたタイプ {#section-6c42b62dd91c4e9bb3a067b9abe3adee}

**アセット**

追加されたパラメータ：

* `readyForPublish`
* `trashState`
* `MaskInfo`
* `RTFInfo`

削除されたパラメータ：

* `ImageSetInfo`
* `RenderSetInfo`

**ReprocessAssetsJob**

追加されたパラメータ：

* `preservePublishState`
* `preserveCrop`
* `readyForPublish`

**UploadDirectoryJob**

追加されたパラメータ：

* `preservePublishState`
* `preserveCrop`
* `videoEncodingPreset`

**UploadUrlsJob**

追加されたパラメータ：

* `preservePublishState`
* `preserveCrop`

