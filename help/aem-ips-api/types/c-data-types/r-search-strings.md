---
description: PDF ファイルから抽出された文字列レコードを検索します。
solution: Experience Manager
title: SearchStrings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 3f67ba8a-12dd-4698-9502-7cbdec9cb25d
TQID: 'https://experienceleague.adobe.com/bWokSVoIEkxrKgXAkaR4ycgSjZAWb2trFnqokTe98XQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 81
ht-degree: 11%

---

# [!DNL SearchStrings]{#searchstrings}

PDF ファイルから抽出された文字列レコードを検索します。

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| searchString | `xsd:string` | 文字列テキストを検索します。 |
| keywordsArray | `types:KeywordsArray` | 検索文字列内のキーワードの配列。 |
| status | `xsd:boolean` | 検索文字列が有効で有効な場合はTrueです。 |
| x | `xsd:int` | 検索文字列のX軸位置。 |
| y | `xsd:int` | 検索文字列のY軸位置。 |
| 幅 | `xsd:int` | 検索文字列の幅。 |
| 高さ | `xsd:int` | 検索文字列の高さ。 |
| fontName | `xsd:string` | 検索文字列で使用されるフォントの名前。 |
| pointSize | `xsd:string` | フォントサイズ： |
