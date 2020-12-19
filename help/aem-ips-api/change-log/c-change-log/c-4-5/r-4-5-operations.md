---
description: IPS APIバージョン4.5の新しい操作方法と変更された操作方法について説明します。
seo-description: IPS APIバージョン4.5の新しい操作方法と変更された操作方法について説明します。
seo-title: 新規および変更された操作
solution: Experience Manager
title: 新規および変更された操作
topic: Scene7 Image Production System API
uuid: c4002670-c830-474e-bb84-343f76b6fb80
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

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

