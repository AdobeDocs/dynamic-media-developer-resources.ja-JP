---
description: ブラウザーでのクリックアクションのターゲットです。
seo-description: ブラウザーでのクリックアクションのターゲットです。
seo-title: 画像マップ
solution: Experience Manager
title: 画像マップ
topic: Scene7 Image Production System API
uuid: 1a09ab27-7ee1-4162-8047-575f3f5ca8fe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 画像マップ{#imagemap}

ブラウザーでのクリックアクションのターゲットです。

常に画像に関連付けられます。 ターゲットを取得 `ImageMap` できます `ImageInfo`。

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| ` *`imageMapHandle`*` | `xsd:string` | 画像マップのハンドル |
| ` *`name`*` | `xsd:string` | 画像マップ名。 |
| ` *`地域`*` | `xsd:string` | 画像マップの座標。 形式はHTMLタグ属性に基づ `<area>` きます。 |
| ` *`action`*` | `xsd:string` | HTMLタグに含めるその他の属 `<area>` 性( `href` URLを含む)。 |
| ` *`shapeType`*` | `xsd:boolean` | 値 [!DNL RegionShape] です。 |
| ` *`掲載順位`*` | `xsd:string` | HTML要素の属性の形式 `<area>` での位 [!DNL coords] 置。 For example: `coords ="0,0,84,128"`. |
| ` *`有効`*` | `xsd:boolean` | 画像マップが有効な場合はtrue。 |
| ` *`lastModified`*` | `xsd:dateTime` | 画像マップが最後に変更された日時。 |

