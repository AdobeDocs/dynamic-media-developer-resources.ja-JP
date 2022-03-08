---
title: AssetContextStateUpdate
description: アセットに関連付けられた公開コンテキストに対して、新しい公開状態フラグのセットを設定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: ecbadafc-e77d-4c7e-a3d5-31c2b2a9b2ea
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 6%

---

# AssetContextStateUpdate{#assetcontextstateupdate}

アセットに関連付けられた公開コンテキストに対して、新しい公開状態フラグのセットを設定します。

**パラメータ**

| 名前 | 種類 | 説明 |
|---|---|---|
| assetHandle | `xsd:string` | 更新するアセットに対してを処理します。 |
| contextStateUpdateArray | `types:ContextStateUpdateArray` | 更新するアセットの公開連絡先の状態の配列。 |
