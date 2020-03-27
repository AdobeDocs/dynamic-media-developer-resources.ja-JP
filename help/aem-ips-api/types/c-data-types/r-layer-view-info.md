---
description: レイヤービューのプロパティ
seo-description: レイヤービューのプロパティ
seo-title: LayerViewInfo
solution: Experience Manager
title: LayerViewInfo
topic: Scene7 Image Production System API
uuid: 58d26f4d-03a6-4f57-bc8e-117355c0d74c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# LayerViewInfo{#layerviewinfo}

レイヤービューのプロパティ

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| ` *`url`*` | `xsd:string` | テンプレートを表すImage ServerのURL。 フィールド `urlModifier` とフィールドを `urlPostAp- plyModifier` 結合します。 |
| ` *`urlModifier`*` | `xsd:string` | 要求またはコマンドの前に適用する画像サービングプロトコルコ `urlPostApplyModifier` マンド。 |
| ` *`urlPostApplyModifier`*` | `xsd:string` | コマンドおよび要求の後に適用する画像サービング `urlModifier` プロトコルコマンド。 |

