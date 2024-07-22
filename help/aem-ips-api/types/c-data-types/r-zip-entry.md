---
description: ZIP ファイルのエントリ。
solution: Experience Manager
title: 郵便番号
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f71f57db-6717-4a27-b275-19bc4cf59ea4
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '42'
ht-degree: 11%

---

# [!DNL ZipEntry]{#zipentry}

ZIP ファイルのエントリ。

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| name | `xsd:string` | エントリ名。 |
| isDirectory | `xsd:boolean` | エントリがディレクトリかどうかを判断します。 |
| lastModified | `xsd:dateTime` | 最終変更日時。 |
| compressedSize | `xsd:long` | 圧縮サイズ。 |
| uncompressedSize | `xsd:long` | 非圧縮サイズ。 |
