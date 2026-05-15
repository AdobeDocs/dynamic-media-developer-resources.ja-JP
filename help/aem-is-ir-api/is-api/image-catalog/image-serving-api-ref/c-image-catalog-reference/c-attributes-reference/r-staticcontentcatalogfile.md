---
description: 静的コンテンツカタログデータファイルのパス。 このカタログの静的コンテンツデータを含むファイルを指定します。
solution: Experience Manager
title: StaticContentCatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ff6f0ad8-189f-4172-89cb-f138d2df8fe4
TQID: 'https://experienceleague.adobe.com/98uNzMz83z3lfa2d3LNixYKZzUWWE9zqrK1fnPo-JNA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 3%

---

# StaticContentCatalogFile{#staticcontentcatalogfile}

静的コンテンツカタログデータファイルのパス。 このカタログの静的コンテンツデータを含むファイルを指定します。

静的コンテンツカタログデータファイルは、指定した順序で読み込まれます。 同じ`static::Id`値が複数のレコード（同じまたは異なるカタログファイル）で発生する場合、最後のインスタンスが優先されます。

## プロパティ {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

1つ以上のテキスト文字列値をコンマで区切ります。 オプション。 各値は、カタログフォルダーに関連する絶対ファイルパスまたはパスである必要があります。

## 初期設定 {#section-702edfbc00c54fc29e412a3ff99fef2b}

空。この画像カタログに静的コンテンツデータが含まれていないことを示します。

## 関連項目 {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[カタログデータ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
