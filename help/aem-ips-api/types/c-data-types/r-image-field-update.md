---
description: 画像アセットに関連付けられている画像フィールドを更新します。
solution: Experience Manager
title: ImageFieldUpdate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82bc016b-8a2b-4811-a0b4-1e2a93add3b6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 11%

---

# ImageFieldUpdate{#imagefieldupdate}

画像アセットに関連付けられている画像フィールドを更新します。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| assetHandle | `xsd:string` | アセットハンドル。 |
| resolution | `xsd:double` | 画像の解像度（ピクセル/インチ）。 |
| anchorX | `xsd:int` | X 軸画像アンカー。 |
| anchorY | `xsd:int` | Y 軸の画像アンカー。 |
| ユーザデータ | `xsd:string` | の値 `userData` 画像サービングユーザーデータカタログフィールドに公開されるメタデータフィールド。 |
