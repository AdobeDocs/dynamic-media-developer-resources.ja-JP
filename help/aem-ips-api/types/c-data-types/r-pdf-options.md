---
description: PDFファイルのオプション
seo-description: PDFファイルのオプション
seo-title: PDFOptions
solution: Experience Manager
title: PDFOptions
uuid: 7558b6b5-ad32-4baf-896b-f4e2bd48f2ec
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 8%

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

