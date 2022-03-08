---
description: ZIP ファイル内のエントリ。
solution: Experience Manager
title: ZipEntry
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f71f57db-6717-4a27-b275-19bc4cf59ea4
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '43'
ht-degree: 13%

---

# ZipEntry{#zipentry}

ZIP ファイル内のエントリ。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| name | `xsd:string` | エントリ名。 |
| isDirectory | `xsd:boolean` | エントリがディレクトリかどうかを判断します。 |
| lastModified | `xsd:dateTime` | 最終変更の日時。 |
| compressedSize | `xsd:long` | 圧縮サイズ。 |
| uncompressedSize | `xsd:long` | 非圧縮サイズ。 |
