---
description: ブラウザーでのクリック操作のターゲット。
solution: Experience Manager
title: 画像マップ
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 10%

---


# 画像マップ{#imagemap}

ブラウザーでのクリック操作のターゲット。

常に画像に関連付けられます。 `ImageInfo`から`ImageMap`ターゲットを取得できます。

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`imageMapHandle`*` | `xsd:string` | 画像マップハンドル |
| `*`name`*` | `xsd:string` | 画像マップ名。 |
| `*`地域`*` | `xsd:string` | 画像マップの座標。 形式は、HTMLの`<area>`タグ属性に基づきます。 |
| `*`action`*` | `xsd:string` | HTML `<area>`タグに含める他の属性（`href` URLを含む）。 |
| `*`shapeType`*` | `xsd:boolean` | [!DNL RegionShape]値。 |
| `*`position`*` | `xsd:string` | HTML `<area>`要素の[!DNL coords]属性の形式での位置。 次に例を示します。`coords ="0,0,84,128"`. |
| `*`有効`*` | `xsd:boolean` | 画像マップが有効な場合はtrue。 |
| `*`lastModified`*` | `xsd:dateTime` | 画像マップが最後に変更された日時。 |

