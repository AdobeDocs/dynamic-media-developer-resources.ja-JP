---
description: レイヤー表示のプロパティ。
seo-description: レイヤー表示のプロパティ。
seo-title: LayerViewInfo
solution: Experience Manager
title: LayerViewInfo
topic: Dynamic Media Image Production System API
uuid: 58d26f4d-03a6-4f57-bc8e-117355c0d74c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 11%

---


# LayerViewInfo{#layerviewinfo}

レイヤー表示のプロパティ。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`url`*` | `xsd:string` | テンプレートを表すImage ServerのURL。 `urlModifier`フィールドと`urlPostAp- plyModifier`フィールドを結合します。 |
| `*`urlModifier`*` | `xsd:string` | 要求または`urlPostApplyModifier`コマンドの前に適用する画像サービングプロトコルコマンド。 |
| `*`urlPostApplyModifier`*` | `xsd:string` | `urlModifier`およびrequestコマンドの後に適用する画像サービングプロトコルコマンド。 |

