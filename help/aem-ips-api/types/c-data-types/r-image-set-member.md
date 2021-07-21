---
description: 画像セットに属するアセット。
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic,SDK/API，画像セット
role: Developer,Admin
exl-id: f0857d98-be79-40a6-8a84-c2c7b4c423c5
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 6%

---

# ImageSetMember{#imagesetmember}

画像セットに属するアセット。

ページのリセットとは、[!DNL eCatalog]が新しいページを開始することを意味します。 `RenderSet` は、スウォッチの一部であることを示 `RenderSet` します。`eCatalog`セットと`RenderSet`セットの値は、強制的に`true`になります。

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`asset`*` | `type:Asset` | 画像セット配列内のアセット。 |
| `*`pageReset`*` | `xsd:boolean` | 新しいページを開始します。 設定は無視され、`eCatalog`セットと`RenderSet`セットの値は強制的に`true`になります。 |
