---
description: ZIPファイル内のエントリ。
seo-description: ZIPファイル内のエントリ。
seo-title: ZipEntry
solution: Experience Manager
title: ZipEntry
topic: Scene7 Image Production System API
uuid: 05aac11b-249c-4c44-943d-fa6bf35d3637
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
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
| ` *`name`*` | `xsd:string` | 参加者名。 |
| ` *`isDirectory`*` | `xsd:boolean` | エントリがディレクトリかどうかを判定します。 |
| ` *`lastModified`*` | `xsd:dateTime` | 最終変更日時。 |
| ` *`compressedSize`*` | `xsd:long` | 圧縮サイズ |
| ` *`uncompressedSize`*` | `xsd:long` | 非圧縮サイズ |

