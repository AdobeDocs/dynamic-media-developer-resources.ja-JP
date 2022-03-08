---
description: ブラウザーでのクリックアクションのターゲットです。
solution: Experience Manager
title: 画像マップ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 11%

---

# 画像マップ{#imagemap}

ブラウザーでのクリックアクションのターゲットです。

常に画像に関連付けられています。 次の情報を取得： `ImageMap` ターゲットから `ImageInfo`.

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| imageMapHandle | `xsd:string` | 画像マップハンドル。 |
| name | `xsd:string` | 画像マップ名。 |
| 地域 | `xsd:string` | 画像マップの座標。 形式はHTML `<area>` タグ属性。 |
| action | `xsd:string` | HTMLに含めるその他の属性 `<area>` タグ ( `href` URL。 |
| shapeType | `xsd:boolean` | A [!DNL RegionShape] の値です。 |
| position | `xsd:string` | HTML `<area>` 要素の [!DNL coords] 属性。 例： `coords ="0,0,84,128"`. |
| 有効 | `xsd:boolean` | 画像マップが有効な場合は true。 |
| lastModified | `xsd:dateTime` | 画像マップが最後に変更された日時。 |
