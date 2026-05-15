---
description: 画像セットに属するAssets。
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: f0857d98-be79-40a6-8a84-c2c7b4c423c5
TQID: 'https://experienceleague.adobe.com/53rc6Cq1i15GdzOpBek7ls7ixq4RN8z0OfZMOZsqYWI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 68
ht-degree: 5%

---

# [!DNL ImageSetMember]{#imagesetmember}

画像セットに属するAssets。

ページのリセットとは、[!DNL eCatalog]が新しいページを開始する必要があることを意味します。 `RenderSet`は、`RenderSet` スウォッチの一部であることを示します。 値は、`eCatalog`および`RenderSet` セットに対して`true`に強制的に設定されます。

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| asset | `type:Asset` | 画像セット配列のAssets。 |
| pageReset | `xsd:boolean` | 新しいページを開始します。 設定は無視され、`eCatalog` セットと`RenderSet` セットでは値が`true`に強制的に設定されます。 |
