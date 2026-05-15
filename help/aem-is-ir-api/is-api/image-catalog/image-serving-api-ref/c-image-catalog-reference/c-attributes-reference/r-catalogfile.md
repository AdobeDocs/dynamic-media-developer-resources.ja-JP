---
description: 画像データファイルのパス。 このカタログの画像データを含むファイルを指定します。
solution: Experience Manager
title: CatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 240a3884-68dd-474c-83a6-d79fc5b6c300
TQID: 'https://experienceleague.adobe.com/MhxEBtyw3JIvMg5miQotPPCeoLeWATtXy0fbRtE7ePs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 108
ht-degree: 3%

---

# CatalogFile{#catalogfile}

画像データファイルのパス。 このカタログの画像データを含むファイルを指定します。

画像データファイルは、指定した順序で読み込まれます。 同じ`catalog::Id`値が複数のレコード（同じまたは異なるカタログファイル）で発生する場合、最後のインスタンスが優先されます。

## プロパティ {#section-6da55f145ecd4e31a5de52637a436983}

1つ以上のテキスト文字列値をコンマで区切ります。 オプション。 各値は、カタログフォルダーに関連する絶対ファイルパスまたはパスである必要があります。

## 初期設定 {#section-80f91cd7a6b2479ebb310319e9c74da7}

空。この画像カタログに画像データが含まれていないことを示します。

## 関連項目 {#section-910b67c5041d44d99a105ad43ff63a37}

[カタログデータフィールド](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
