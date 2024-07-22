---
description: 画像アセットに関連付けられた画像フィールドを更新します。
solution: Experience Manager
title: ImageFieldUpdate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82bc016b-8a2b-4811-a0b4-1e2a93add3b6
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 7%

---

# [!DNL ImageFieldUpdate]{#imagefieldupdate}

画像アセットに関連付けられた画像フィールドを更新します。

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| assetHandle | `xsd:string` | アセットハンドル。 |
| [!DNL resolution] | `xsd:double` | 画像の解像度（1 インチあたりのピクセル数）。 |
| [!DNL anchorX] | `xsd:int` | X 軸画像アンカー。 |
| [!DNL anchorY] | `xsd:int` | Y 軸画像アンカー。 |
| [!DNL userData] | `xsd:string` | 画像サ `userData` ビスユーザーデータカタログフィールドに公開されるメタデータフィールドの値。 |
