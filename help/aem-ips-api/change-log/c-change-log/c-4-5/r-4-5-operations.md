---
description: IPS API バージョン 4.5 の新しい操作方法および変更された操作方法について説明します。
solution: Experience Manager
title: 操作 — 新規および変更済み
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9033328a-d0ce-4ef2-b6ec-c6a81fbedf9d
source-git-commit: 10eb6887663fe335be3abcc311b2d3eb4a241745
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 1%

---

# 操作：新規および変更済み{#operations-new-and-modified}

IPS API バージョン 4.5 の新しい操作方法および変更された操作方法について説明します。

構文

## 新しい操作 {#section-a3be679d8e9345aba2e97699c3a537b9}

* `addMediaPortalEvent`
* `addTagFieldValues`
* `cdnCacheInvalidation`
* `deleteTagFieldValues`
* `deleteTagFieldValues`
* `getDistinctMetadataValues`
* `getMediaPortalEvent`
* `getTagFieldValues`
* `getXMPPacket`
* `searchAssetsByFullText`
* `searchAssetsByMetadata`
* `setTagFieldValues`
* `updateTagFieldValues`
* `updateXMPPacket`

## 変更された操作 {#section-1c022cc62d274c349837013f1c02ca51}

* `Asset` 次を含む `animatedGifInfo`, `swcInfo`, `cssInfo`、および `javascriptInfo` パラメーター。
* `createMetadataField` オプションの `isHidden` パラメーター。
* `saveMetadataField` オプションの `isHidden` パラメーター。
* `searchAssets`
* この `renameFiles` パラメーターは以前のリリースで非推奨となり、から削除されました `renameAsset` 操作。 仮想ファイルのパスは、新しいアセット名（ファイル拡張子を維持）に一致するように変更されますが、物理ファイルのパスは影響を受けません。 API クライアントは、新しい API バージョンに更新する際に、このパラメーターへの参照を削除する必要があります。
