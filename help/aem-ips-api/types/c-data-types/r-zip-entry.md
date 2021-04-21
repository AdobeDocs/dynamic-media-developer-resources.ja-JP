---
description: ZIPファイル内のエントリ。
solution: Experience Manager
title: ZipEntry
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 12%

---


# ZipEntry{#zipentry}

ZIPファイル内のエントリ。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`name`*` | `xsd:string` | 参加者名。 |
| `*`isDirectory`*` | `xsd:boolean` | エントリがディレクトリかどうかを判定します。 |
| `*`lastModified`*` | `xsd:dateTime` | 最終変更日時。 |
| `*`compressedSize`*` | `xsd:long` | 圧縮サイズ |
| `*`uncompressedSize`*` | `xsd:long` | 非圧縮サイズ |

