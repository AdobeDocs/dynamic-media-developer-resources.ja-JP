---
description: PostScriptのファイルオプション。
solution: Experience Manager
title: PostScriptOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fd2093b5-9856-4f31-8853-1027194a71df
TQID: 'https://experienceleague.adobe.com/XsIiYor0c-7I34OYazNaSF0Hx3sbZmzpTzAT1u73xxo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 65
ht-degree: 10%

---

# [!DNL PostScriptOptions]{#postscriptoptions}

PostScriptのファイルオプション。

構文

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| プロセス | `xsd:string` | PostScriptプロセスの選択： |
| resolution | `xsd:double` | ファイル解決： |
| 色空間 | `xsd:string` | PostScript カラースペースモード。 |
| 英 | `xsd:boolean` | ファイルを画像にラスタライズするかどうか。 その場合、元のファイルがこのように定義されている場合は、透明な背景が作成されます。 一般的に、オーバーレイのロゴを作成するために使用されます。 |
| extractSearchWords | `xsd:boolean` | PostScript ファイルから検索語を抽出するかどうか。 |
