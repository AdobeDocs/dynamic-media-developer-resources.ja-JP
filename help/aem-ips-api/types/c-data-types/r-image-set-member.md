---
description: 画像セットに属するアセット。
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: f0857d98-be79-40a6-8a84-c2c7b4c423c5
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 7%

---

# [!DNL ImageSetMember]{#imagesetmember}

画像セットに属するアセット。

ページのリセットとは、 [!DNL eCatalog] が新しいページを開始する必要があります。 `RenderSet` これが `RenderSet` スウォッチ 値は、強制的に次のようになります。 `true` 対象 `eCatalog` および `RenderSet` セット。

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| asset | `type:Asset` | 画像セット配列内のアセット。 |
| pageReset | `xsd:boolean` | 新しいページを開始します。 設定は無視され、値は強制的に `true` 対象 `eCatalog` および `RenderSet` セット。 |
