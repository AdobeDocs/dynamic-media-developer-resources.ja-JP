---
description: ブラウザー内のクリック操作のターゲット定義。
seo-description: ブラウザー内のクリック操作のターゲット定義。
seo-title: ImageMapDefinition
solution: Experience Manager
title: ImageMapDefinition
topic: Scene7 Image Production System API
uuid: e3b9a304-5c43-46ce-8e87-860b49006a37
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 10%

---


# ImageMapDefinition{#imagemapdefinition}

ブラウザー内のクリック操作のターゲット定義。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| ` *`name`*` | `xsd:string` | 画像マップ定義の名前。 |
| ` *`shapeType`*` | `xsd:string` | 領域形状の値の1つ。 |
| ` *`地域`*` | `xsd:string` | 画像マップの座標。 形式は、HTMLの`<area>`タグ属性に基づきます。 |
| ` *`action`*` | `xsd:string` | HTML `<area>`タグに含める他の属性（`href` URLを含む）。 |
| ` *`有効`*` | `xsd:boolean` | 画像マップが有効な場合はtrue。 |

