---
description: ZIPファイル内のエントリ。
solution: Experience Manager
title: ZipEntry
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
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

