---
description: 画像アセットに関連付けられている画像フィールドを更新します。
solution: Experience Manager
title: ImageFieldUpdate
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 8%

---


# ImageFieldUpdate{#imagefieldupdate}

画像アセットに関連付けられている画像フィールドを更新します。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | アセットハンドル |
| `*`resolution`*` | `xsd:double` | 画像解像度（ピクセル/インチ）。 |
| `*`anchorX`*` | `xsd:int` | X軸の画像アンカー |
| `*`anchorY`*` | `xsd:int` | Y軸の画像アンカー |
| `*`ユーザデータ`*` | `xsd:string` | `userData`メタデータフィールドの値。画像サービングのユーザデータカタログフィールドに発行されます。 |

