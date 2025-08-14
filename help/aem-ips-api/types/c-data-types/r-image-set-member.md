---
description: 画像セットに属するAssets。
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: f0857d98-be79-40a6-8a84-c2c7b4c423c5
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 5%

---

# [!DNL ImageSetMember]{#imagesetmember}

画像セットに属するAssets。

ページリセットとは、[!DNL eCatalog] ーザーが新しいページを開始する必要があることを意味します。 `RenderSet` は、`RenderSet` スウォッチの一部であることを示します。 値は、`true` と `eCatalog` のセットに対して強制的に `RenderSet` されます。

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| asset | `type:Asset` | 画像セット配列内のAssets |
| pageReset | `xsd:boolean` | 新しいページを開始します。 の設定は無視され、`true` セットと `eCatalog` セットの場合は値が強制的に `RenderSet` になります。 |
