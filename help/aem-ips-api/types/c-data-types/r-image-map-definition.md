---
description: ブラウザー内のクリック操作のターゲット定義。
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 11%

---


# ImageMapDefinition{#imagemapdefinition}

ブラウザー内のクリック操作のターゲット定義。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`name`*` | `xsd:string` | 画像マップ定義の名前。 |
| `*`shapeType`*` | `xsd:string` | 領域形状の値の1つ。 |
| `*`地域`*` | `xsd:string` | 画像マップの座標。 形式は、HTMLの`<area>`タグ属性に基づきます。 |
| `*`action`*` | `xsd:string` | HTML `<area>`タグに含める他の属性（`href` URLを含む）。 |
| `*`有効`*` | `xsd:boolean` | 画像マップが有効な場合はtrue。 |

