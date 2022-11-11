---
description: PDFファイルオプション
solution: Experience Manager
title: PDFOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 140c9261-e590-4889-9be4-29afd19ffa86
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 11%

---

# [!DNL PDFOptions]{#pdfoptions}

PDFファイルオプション

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| プロセス | `xsd:string` | 「PDFプロセス」の選択 |
| resolution | `xsd:double` | ファイルの解像度。 |
| カラースペース | `xsd:string` | ポストスクリプトカラースペースモードの選択。 |
| pdfCatalog | `xsd:boolean` | レンダリング後に複数のページPDFを eCatalog に組み合わせるかどうか（デフォルトは true）。 |
| extractSearchWords | `xsd:boolean` | 検索語を抽出ファイルからPDFするか。 |
| extractLinks | `xsd:boolean` | IPS 内のラスタライズされたページに割り当てられたPDFマップに画像リンクを抽出するかどうか。 |
