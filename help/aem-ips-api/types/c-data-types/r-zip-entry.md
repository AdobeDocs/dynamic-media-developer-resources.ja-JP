---
description: ZIPファイル内のエントリ。
seo-description: ZIPファイル内のエントリ。
seo-title: ZipEntry
solution: Experience Manager
title: ZipEntry
uuid: 05aac11b-249c-4c44-943d-fa6bf35d3637
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 10%

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

