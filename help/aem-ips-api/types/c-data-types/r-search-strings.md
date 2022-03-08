---
description: 検索ファイルから抽出した検索PDFレコード。
solution: Experience Manager
title: SearchStrings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 3f67ba8a-12dd-4698-9502-7cbdec9cb25d
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 12%

---

# SearchStrings{#searchstrings}

検索ファイルから抽出した検索PDFレコード。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| searchString | `xsd:string` | 検索文字列テキスト。 |
| keywordsArray | `types:KeywordsArray` | 検索文字列内のキーワードの配列。 |
| status | `xsd:boolean` | 検索文字列が有効で有効な場合は true。 |
| x | `xsd:int` | 検索文字列の X 軸位置。 |
| y | `xsd:int` | 検索文字列の Y 軸の位置。 |
| 幅 | `xsd:int` | 検索文字列の幅。 |
| 高さ | `xsd:int` | 検索文字列の高さ。 |
| fontName | `xsd:string` | 検索文字列で使用されるフォントの名前。 |
| pointSize | `xsd:string` | フォントサイズ。 |
