---
description: ブラウザーでのクリックアクションのターゲットです。
solution: Experience Manager
title: 画像マップ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 5%

---

# [!DNL ImageMap]{#imagemap}

ブラウザーでのクリックアクションのターゲットです。

常に画像に関連付けられています。 次の情報を取得： `ImageMap` ターゲットから `ImageInfo`.

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| imageMapHandle | `xsd:string` | 画像マップハンドル。 |
| [!DNL name] | `xsd:string` | 画像マップ名。 |
| [!DNL region] | `xsd:string` | 画像マップの座標。 形式はHTML `<area>` タグ属性。 |
| [!DNL action] | `xsd:string` | HTMLに含めるその他の属性 `<area>` タグ ( `href` URL。 |
| shapeType | `xsd:boolean` | A [!DNL RegionShape] の値です。 |
| [!DNL position] | `xsd:string` | HTML `<area>` 要素の [!DNL coords] 属性。 例： `coords ="0,0,84,128"`. |
| [!DNL enabled] | `xsd:boolean` | 画像マップが有効な場合は true。 |
| lastModified | `xsd:dateTime` | 画像マップが最後に変更された日時。 |
