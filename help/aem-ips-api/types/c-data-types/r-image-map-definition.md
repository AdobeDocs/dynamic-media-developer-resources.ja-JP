---
description: ブラウザーでのクリックアクションのターゲット定義。
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 58478e7c-e3a1-4dd5-8ff9-e9752301b93c
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 11%

---

# ImageMapDefinition{#imagemapdefinition}

ブラウザーでのクリックアクションのターゲット定義。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`name`*` | `xsd:string` | 画像マップ定義の名前。 |
| `*`shapeType`*` | `xsd:string` | 領域の形状値の1つ。 |
| `*`地域`*` | `xsd:string` | 画像マップの座標。 形式は、HTMLの`<area>`タグ属性に基づきます。 |
| `*`action`*` | `xsd:string` | HTMLの`<area>`タグに含める他の属性（`href` URLを含む）。 |
| `*`有効`*` | `xsd:boolean` | 画像マップが有効な場合はtrue。 |
