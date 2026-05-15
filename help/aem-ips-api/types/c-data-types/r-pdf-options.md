---
description: PDFのファイルオプション。
solution: Experience Manager
title: PDFOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 140c9261-e590-4889-9be4-29afd19ffa86
TQID: 'https://experienceleague.adobe.com/gjd-g7jhWVbLRL3kYnkX96ihjkiK34oCp7Ns1iC89GM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 68
ht-degree: 8%

---

# [!DNL PDFOptions]{#pdfoptions}

PDFのファイルオプション。

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| プロセス | `xsd:string` | 「PDF プロセス」の選択。 |
| resolution | `xsd:double` | ファイル解決： |
| 色空間 | `xsd:string` | スクリプト後のカラースペースモードの選択。 |
| pdfCatalog | `xsd:boolean` | レンダリング後に複数ページのPDFをeCatalogに組み合わせるかどうか（デフォルトはtrue）。 |
| extractSearchWords | `xsd:boolean` | PDF ファイルから検索語を抽出するかどうか。 |
| extractLinks | `xsd:boolean` | IPS内のラスタライズされたページに割り当てられた画像マップにPDF リンクを抽出するかどうか。 |
