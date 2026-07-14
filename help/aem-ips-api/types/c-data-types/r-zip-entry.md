---
description: ZIP ファイルのエントリ。
solution: Experience Manager
title: ZipEntry
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f71f57db-6717-4a27-b275-19bc4cf59ea4
TQID: 'https://experienceleague.adobe.com/u8w7i9pPiCJTkbxwQXg-IBIz3hDWtxrEvqNJ5JERM64'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 42
ht-degree: 11%

---

# [!DNL ZipEntry]{#zipentry}

ZIP ファイルのエントリ。

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| name | `xsd:string` | エントリ名。 |
| isDirectory | `xsd:boolean` | エントリがディレクトリであるかどうかを指定します。 |
| lastModified | `xsd:dateTime` | 最終変更日時。 |
| compressedSize | `xsd:long` | 圧縮サイズ。 |
| uncompressedSize | `xsd:long` | 非圧縮サイズ。 |

