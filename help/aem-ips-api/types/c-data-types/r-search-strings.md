---
description: PDFファイルから抽出された検索文字列レコード。
solution: Experience Manager
title: SearchStrings
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 3f67ba8a-12dd-4698-9502-7cbdec9cb25d
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 11%

---

# SearchStrings{#searchstrings}

PDFファイルから抽出された検索文字列レコード。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`searchString`*` | `xsd:string` | 検索文字列のテキスト。 |
| `*`keywordsArray`*` | `types:KeywordsArray` | 検索文字列内のキーワードの配列。 |
| `*`status`*` | `xsd:boolean` | 検索文字列が有効で有効な場合はtrue。 |
| `*`x`*` | `xsd:int` | 検索文字列のX軸位置。 |
| `*`y`*` | `xsd:int` | 検索文字列のY軸位置。 |
| `*`width`*` | `xsd:int` | 検索文字列の幅。 |
| `*`height`*` | `xsd:int` | 検索文字列の高さ。 |
| `*`fontName`*` | `xsd:string` | 検索文字列で使用されるフォントの名前。 |
| `*`pointSize`*` | `xsd:string` | フォントサイズ |
