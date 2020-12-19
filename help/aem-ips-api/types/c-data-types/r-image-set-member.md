---
description: 画像セットに属するアセット。
seo-description: 画像セットに属するアセット。
seo-title: ImageSetMember
solution: Experience Manager
title: ImageSetMember
topic: Scene7 Image Production System API
uuid: bd013609-aed7-4c85-80f9-16be7fce99a3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 6%

---


# ImageSetMember{#imagesetmember}

画像セットに属するアセット。

ページのリセットとは、[!DNL eCatalog]が新しいページを開始する必要があることを意味します。 `RenderSet` は、そのスウォッチが `RenderSet` スウォッチの一部であることを示します。`eCatalog`と`RenderSet`セットの値は強制的に`true`になります。

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| ` *`asset`*` | `type:Asset` | 画像セット配列内のアセット。 |
| ` *`pageReset`*` | `xsd:boolean` | 新しいページを開始します。 設定は無視され、`eCatalog`と`RenderSet`のセットの値は強制的に`true`に設定されます。 |

