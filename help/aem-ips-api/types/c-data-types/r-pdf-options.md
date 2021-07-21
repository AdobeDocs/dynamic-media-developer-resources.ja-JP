---
description: PDFファイルのオプション
solution: Experience Manager
title: PDFOptions
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 140c9261-e590-4889-9be4-29afd19ffa86
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 9%

---

# PDFOptions{#pdfoptions}

PDFファイルのオプション

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`プロセス`*` | `xsd:string` | 「PDFプロセス」の選択 |
| `*`resolution`*` | `xsd:double` | ファイルの解像度。 |
| `*`カラースペース`*` | `xsd:string` | ポストスクリプトカラースペースモードを選択します。 |
| `*`pdfCatalog`*` | `xsd:boolean` | レンダリング後に複数ページのPDFをeCatalogに結合するかどうか（デフォルトはtrue）。 |
| `*`extractSearchWords`*` | `xsd:boolean` | PDFファイルから検索語を抽出するかどうか。 |
| `*`extractLinks`*` | `xsd:boolean` | IPS内のラスタライズされたページに割り当てられた画像マップにPDFリンクを抽出するかどうか。 |
