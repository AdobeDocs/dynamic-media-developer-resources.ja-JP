---
description: 画像アセットに関連付けられている画像フィールドを更新します。
solution: Experience Manager
title: ImageFieldUpdate
feature: Dynamic Media Classic、SDK/API
role: Developer,Administrator
exl-id: 82bc016b-8a2b-4811-a0b4-1e2a93add3b6
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 9%

---

# ImageFieldUpdate{#imagefieldupdate}

画像アセットに関連付けられている画像フィールドを更新します。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | アセットハンドル。 |
| `*`resolution`*` | `xsd:double` | 画像の解像度（ピクセル/インチ）。 |
| `*`anchorX`*` | `xsd:int` | X軸イメージアンカー |
| `*`anchorY`*` | `xsd:int` | Y軸イメージアンカー |
| `*`ユーザデータ`*` | `xsd:string` | `userData`メタデータフィールドの値。画像サービングのユーザーデータカタログフィールドに公開されます。 |
