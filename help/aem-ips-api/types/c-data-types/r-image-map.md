---
description: ブラウザーでのクリックアクションのターゲット。
solution: Experience Manager
title: ImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 3%

---

# [!DNL ImageMap]{#imagemap}

ブラウザーでのクリックアクションのターゲット。

常に画像に関連付けられます。 `ImageInfo` から `ImageMap` ターゲットを取得できます。

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| imageMapHandle | `xsd:string` | 画像マップのハンドル。 |
| [!DNL name] | `xsd:string` | 画像マップ名。 |
| [!DNL region] | `xsd:string` | 画像マップの座標。 フォーマットは、タグ属性 `<area>`HTMLに基づいています。 |
| [!DNL action] | `xsd:string` | HTML `<area>` タグに含めるその他の属性（`href` URL など）。 |
| shapeType | `xsd:boolean` | [!DNL RegionShape] 値。 |
| [!DNL position] | `xsd:string` | 要素の [!DNL coords] 属性のHTML`<area>` フォーマット内の位置。 例：`coords ="0,0,84,128"`。 |
| [!DNL enabled] | `xsd:boolean` | True を指定すると、イメージ マップが有効になります。 |
| lastModified | `xsd:dateTime` | 画像マップが最後に変更された日時。 |
