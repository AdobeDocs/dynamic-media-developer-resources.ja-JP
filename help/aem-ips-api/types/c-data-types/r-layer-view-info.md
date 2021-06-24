---
description: 画層ビューのプロパティ
solution: Experience Manager
title: LayerViewInfo
feature: Dynamic Media Classic、SDK/API
role: Developer,Administrator
exl-id: 25199c86-1df0-41af-b210-e7668a60295e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 11%

---

# LayerViewInfo{#layerviewinfo}

画層ビューのプロパティ

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`url`*` | `xsd:string` | テンプレートを表す画像サーバーのURL。 `urlModifier`フィールドと`urlPostAp- plyModifier`フィールドを組み合わせます。 |
| `*`urlModifier`*` | `xsd:string` | 要求または`urlPostApplyModifier`コマンドの前に適用する画像サービングプロトコルコマンド。 |
| `*`urlPostApplyModifier`*` | `xsd:string` | `urlModifier`の後に適用する画像サービングプロトコルコマンドと、コマンドを要求します。 |
