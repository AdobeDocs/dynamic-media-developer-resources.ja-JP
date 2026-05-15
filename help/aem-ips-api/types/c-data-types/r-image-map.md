---
description: ブラウザーのクリックアクションのターゲット。
solution: Experience Manager
title: ImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
TQID: 'https://experienceleague.adobe.com/ikMxCQ23L0HzbfmRlcYGL-fRJFK2uhwbZHNzcy1c25k'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 91
ht-degree: 3%

---

# [!DNL ImageMap]{#imagemap}

ブラウザーのクリックアクションのターゲット。

常に画像に関連付けられます。 `ImageInfo`から`ImageMap` ターゲットを取得できます。

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| imageMapHandle | `xsd:string` | 画像マップハンドル。 |
| [!DNL name] | `xsd:string` | 画像マップ名。 |
| [!DNL region] | `xsd:string` | 画像マップ座標。 形式は、HTML `<area>` タグ属性に基づいています。 |
| [!DNL action] | `xsd:string` | HTML `<area>` タグに含めるその他の属性（`href` URLなど）。 |
| shapeType | `xsd:boolean` | [!DNL RegionShape]値。 |
| [!DNL position] | `xsd:string` | HTML `<area>`要素の[!DNL coords]属性の書式の位置。 例：`coords ="0,0,84,128"`。 |
| [!DNL enabled] | `xsd:boolean` | 画像マップが有効な場合はTrueです。 |
| lastModified | `xsd:dateTime` | 画像マップが最後に変更された日時。 |
