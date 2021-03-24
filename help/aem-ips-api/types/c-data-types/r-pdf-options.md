---
description: PDFファイルのオプション
solution: Experience Manager
title: PDFOptions
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '75'
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
| `*`カラースペース`*` | `xsd:string` | ポストスクリプトカラースペースモードの選択 |
| `*`pdfCatalog`*` | `xsd:boolean` | レンダリング後に複数ページのPDFをeCatalogに結合するかどうか（デフォルトはtrue）。 |
| `*`extractSearchWords`*` | `xsd:boolean` | PDFファイルから検索語を抽出するかどうか。 |
| `*`extractLinks`*` | `xsd:boolean` | IPS内のラスタライズページに割り当てられた画像マップにPDFリンクを抽出するかどうか。 |

