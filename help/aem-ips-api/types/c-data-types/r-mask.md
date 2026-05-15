---
description: 画像の一部をマスクします。 マスクは常に画像に関連付けられます。 ImageInfoからマスクを取得します。
solution: Experience Manager
title: マスク
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0e18096c-0666-400b-a562-b6d183bd3334
TQID: 'https://experienceleague.adobe.com/Y4-bWzjkqRASemoKbjKAaDOqewpNmI4AGte-D3TemrY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 69
ht-degree: 7%

---

# [!DNL Mask]{#mask}

画像の一部をマスクします。 マスクは常に画像に関連付けられます。 ImageInfoからマスクを取得します。

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| maskHandle | `xsd:string` | マスクハンドル。 |
| name | `xsd:string` | マスク名。 |
| maskPath | `xsd:string` | マスクの相対パス。 |
| maskFile | `xsd:string` | マスクファイル。 |
| lastModified | `types:dateTime` | マスクが最後に変更された日付、時刻、タイムゾーン。 |
