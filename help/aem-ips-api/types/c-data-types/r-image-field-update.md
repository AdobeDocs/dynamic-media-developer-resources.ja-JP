---
description: 画像アセットに関連付けられている画像フィールドを更新します。
seo-description: 画像アセットに関連付けられている画像フィールドを更新します。
seo-title: ImageFieldUpdate
solution: Experience Manager
title: ImageFieldUpdate
topic: Scene7 Image Production System API
uuid: 0262be3e-f840-41cd-bedc-cc37d9982235
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 8%

---


# ImageFieldUpdate{#imagefieldupdate}

画像アセットに関連付けられている画像フィールドを更新します。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | アセットハンドル |
| ` *`resolution`*` | `xsd:double` | 画像解像度（ピクセル/インチ）。 |
| ` *`anchorX`*` | `xsd:int` | X軸の画像アンカー |
| ` *`anchorY`*` | `xsd:int` | Y軸の画像アンカー |
| ` *`ユーザデータ`*` | `xsd:string` | `userData`メタデータフィールドの値。画像サービングのユーザデータカタログフィールドに発行されます。 |

