---
description: IPS API バージョン 4.5 の新しい操作メソッドと変更された操作メソッドについて説明します。
solution: Experience Manager
title: 操作 – 新規および変更済み
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9033328a-d0ce-4ef2-b6ec-c6a81fbedf9d
source-git-commit: 10eb6887663fe335be3abcc311b2d3eb4a241745
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 1%

---

# 操作：新規および変更{#operations-new-and-modified}

IPS API バージョン 4.5 の新しい操作メソッドと変更された操作メソッドについて説明します。

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

* `Asset` には、`animatedGifInfo`、`swcInfo`、`cssInfo`、`javascriptInfo` のパラメーターが含まれます。
* `createMetadataField` には、オプションの `isHidden` パラメーターが含まれています。
* `saveMetadataField` には、オプションの `isHidden` パラメーターが含まれています。
* `searchAssets`
* `renameFiles` パラメーターは以前のリリースで非推奨（廃止予定）となり、`renameAsset` 操作から削除されました。 仮想ファイルパスは、新しいアセット名に一致するように（ファイルの拡張子は維持されて）変更されますが、物理ファイルパスは影響を受けません。 API クライアントは、新しい API バージョンに更新する際に、このパラメーターへの参照を削除する必要があります。
