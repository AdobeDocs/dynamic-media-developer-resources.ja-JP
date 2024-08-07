---
description: ブラウザーでのクリックアクションのターゲット定義。
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 58478e7c-e3a1-4dd5-8ff9-e9752301b93c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 11%

---

# [!DNL ImageMapDefinition]{#imagemapdefinition}

ブラウザーでのクリックアクションのターゲット定義。

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| name | `xsd:string` | 画像マップ定義の名前。 |
| shapeType | `xsd:string` | 領域シェイプ値の 1 つ。 |
| 地域 | `xsd:string` | 画像マップの座標。 形式は、タグ属性 `<area>`HTMLに基づきます。 |
| action | `xsd:string` | HTML `<area>` タグに含めるその他の属性（`href` URL など）。 |
| 有効 | `xsd:boolean` | 画像マップが有効な場合は true。 |
