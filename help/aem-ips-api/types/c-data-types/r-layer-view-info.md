---
description: レイヤー表示のプロパティ。
solution: Experience Manager
title: LayerViewInfo
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '54'
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

