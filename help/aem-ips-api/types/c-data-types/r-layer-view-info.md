---
description: 画層ビューのプロパティ。
solution: Experience Manager
title: LayerViewInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 25199c86-1df0-41af-b210-e7668a60295e
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 12%

---

# LayerViewInfo{#layerviewinfo}

画層ビューのプロパティ。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| url | `xsd:string` | テンプレートを表す Image Server URL。 結合 `urlModifier` および `urlPostAp- plyModifier` フィールド。 |
| urlModifier | `xsd:string` | 要求または要求の前に適用する画像サービングプロトコルコマンド `urlPostApplyModifier` コマンド |
| urlPostApplyModifier | `xsd:string` | 後に適用する画像サービングプロトコルコマンド `urlModifier` およびリクエストコマンド |
