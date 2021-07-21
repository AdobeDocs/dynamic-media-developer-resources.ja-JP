---
description: アセットに関連付けられた公開コンテキストに対して、公開状態フラグの新しいセットを設定します。
solution: Experience Manager
title: AssetContextStateUpdate
feature: Dynamic Media Classic,SDK/API，アセット管理
role: Developer,Admin
exl-id: ecbadafc-e77d-4c7e-a3d5-31c2b2a9b2ea
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 5%

---

# AssetContextStateUpdate{#assetcontextstateupdate}

アセットに関連付けられた公開コンテキストに対して、公開状態フラグの新しいセットを設定します。

**パラメータ**

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 更新するアセットに対してを処理します。 |
| `*`contextStateUpdateArray`*` | `types:ContextStateUpdateArray` | 更新するアセットの公開連絡先の状態の配列。 |
