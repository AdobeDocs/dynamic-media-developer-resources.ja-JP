---
description: IPS APIバージョン4.5の新しい操作方法と変更された操作方法について説明します。
solution: Experience Manager
title: 新規および変更された操作
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 9033328a-d0ce-4ef2-b6ec-c6a81fbedf9d
source-git-commit: d2e73ae5f92d9ba3471dc7207842753ccff94c28
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---

# 操作：新規および変更済み{#operations-new-and-modified}

IPS APIバージョン4.5の新しい操作方法と変更された操作方法について説明します。

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

* `Asset` には、 `animatedGifInfo`、、および `swcInfo`の各パ `cssInfo`ラメーターが含ま `javascriptInfo` れます。
* `createMetadataField` には、オプションのパラメーターが含 `isHidden` まれています。
* `saveMetadataField` には、オプションのパラメーターが含 `isHidden` まれています。
* `searchAssets`
* `renameFiles`パラメーターは以前のリリースでは廃止され、`renameAsset`操作から削除されました。 仮想ファイルのパスは、新しいアセット名（ファイル拡張子を維持）に一致するように変更されますが、物理ファイルのパスは影響を受けません。 APIクライアントは、新しいAPIバージョンに更新する際に、このパラメーターへの参照を削除する必要があります。
