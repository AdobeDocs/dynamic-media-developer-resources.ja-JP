---
description: PDF ファイルオプション。
solution: Experience Manager
title: PDFOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 140c9261-e590-4889-9be4-29afd19ffa86
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 8%

---

# [!DNL PDFOptions]{#pdfoptions}

PDF ファイルオプション。

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| プロセス | `xsd:string` | 「PDF プロセス」の選択。 |
| resolution | `xsd:double` | ファイルの解像度。 |
| 色空間 | `xsd:string` | ポストスクリプトのカラースペースモードの選択。 |
| pdfCatalog | `xsd:boolean` | レンダリング後に複数ページのPDFを eCatalog に組み合わせるかどうか（デフォルトは true）。 |
| extractSearchWords | `xsd:boolean` | 検索単語をPDF ファイルから抽出するかどうか。 |
| extractLinks | `xsd:boolean` | IPS 内でラスタライズされたページに割り当てられた画像マップにPDF リンクを抽出するかどうかを指定します。 |
