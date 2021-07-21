---
description: ZIPファイル内のエントリ。
solution: Experience Manager
title: ZipEntry
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: f71f57db-6717-4a27-b275-19bc4cf59ea4
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 12%

---

# ZipEntry{#zipentry}

ZIPファイル内のエントリ。

構文

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`name`*` | `xsd:string` | 参加者名。 |
| `*`isDirectory`*` | `xsd:boolean` | エントリがディレクトリかどうかを判断します。 |
| `*`lastModified`*` | `xsd:dateTime` | 最終変更の日時。 |
| `*`compressedSize`*` | `xsd:long` | 圧縮サイズ |
| `*`uncompressedSize`*` | `xsd:long` | 非圧縮サイズ。 |
