---
description: ブラウザーでのクリックアクションのターゲット定義。
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 58478e7c-e3a1-4dd5-8ff9-e9752301b93c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 12%

---

# ImageMapDefinition{#imagemapdefinition}

ブラウザーでのクリックアクションのターゲット定義。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| name | `xsd:string` | 画像マップ定義の名前。 |
| shapeType | `xsd:string` | 領域の形状値の 1 つ。 |
| 地域 | `xsd:string` | 画像マップの座標。 形式はHTML `<area>` タグ属性。 |
| action | `xsd:string` | HTMLに含めるその他の属性 `<area>` タグ ( `href` URL。 |
| 有効 | `xsd:boolean` | 画像マップが有効な場合は true。 |
