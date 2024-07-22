---
title: AssetContextStateUpdate
description: アセットに関連付けられた公開コンテキストに新しい公開状態フラグのセットを設定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: ecbadafc-e77d-4c7e-a3d5-31c2b2a9b2ea
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 4%

---

# [!DNL AssetContextStateUpdate]{#assetcontextstateupdate}

アセットに関連付けられた公開コンテキストに新しい公開状態フラグのセットを設定します。

**パラメーター**

| 名前 | 種類 | 説明 |
|---|---|---|
| assetHandle | `xsd:string` | 更新するアセットへのハンドル。 |
| contextStateUpdateArray | `types:ContextStateUpdateArray` | 更新するアセットの公開問い合わせ先の状態の配列。 |
