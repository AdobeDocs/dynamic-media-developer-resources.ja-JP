---
description: IPS APIバージョン4.5の新しい操作方法と変更された操作方法について説明します。
solution: Experience Manager
title: 新規および変更された操作
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 1%

---


# 操作：新規および変更済み{#operations-new-and-modified}

IPS APIバージョン4.5の新しい操作方法と変更された操作方法について説明します。

構文

## 新しい操作{#section-a3be679d8e9345aba2e97699c3a537b9}

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

## 変更された操作{#section-1c022cc62d274c349837013f1c02ca51}

* `Asset` 含 `animatedGifInfo`む、 `swcInfo`、 `cssInfo`および `javascriptInfo` パラメーター

* `createMetadataField` には、オプションの `isHidden` パラメーターが含まれます。

* `saveMetadataField` には、オプションの `isHidden` パラメーターが含まれます。

* `searchAssets`
* 
* `renameFiles`パラメーターは以前のリリースでは廃止され、`renameAsset`操作から削除されました。 仮想ファイルのパスは、新しいアセット名（ファイル拡張子を保持）に一致するように変更されますが、物理ファイルのパスは影響を受けません。 APIクライアントは、新しいAPIバージョンに更新する際に、このパラメーターへの参照を削除する必要があります。

