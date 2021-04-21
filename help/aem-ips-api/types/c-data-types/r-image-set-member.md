---
description: 画像セットに属するアセット。
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 6%

---


# ImageSetMember{#imagesetmember}

画像セットに属するアセット。

ページのリセットとは、[!DNL eCatalog]が新しいページを開始する必要があることを意味します。 `RenderSet` は、そのスウォッチが `RenderSet` スウォッチの一部であることを示します。`eCatalog`と`RenderSet`セットの値は強制的に`true`になります。

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`asset`*` | `type:Asset` | 画像セット配列内のアセット。 |
| `*`pageReset`*` | `xsd:boolean` | 新しいページを開始します。 設定は無視され、`eCatalog`と`RenderSet`のセットの値は強制的に`true`に設定されます。 |

