---
description: 画像サービングは、ISO-8859-1 および UTF-8 エンコーディングの画像カタログをサポートします。
solution: Experience Manager
title: 文字エンコーディング
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e6e50c2a-53d3-4776-a3f6-4a9d3407e562
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# 文字エンコーディング{#character-encoding}

画像サービングは、ISO-8859-1 および UTF-8 エンコーディングの画像カタログをサポートします。

各ファイルのエンコードを指定するには、バイト順マーク （BOM）を使用します。 UTF-8 の場合、BOM はバイト シーケンス `EF BB BF` です。 UTF-8 エンコーディングは、この文字シーケンスが各画像カタログファイルの先頭で検出された場合に想定されます。 その他のバイトシーケンスの場合、ファイルは ISO-8859-1 規格にエンコードされたものとして解釈されます。

最新のアプリケーションの多くは、UTF-8 で設定されている場合、自動的に BOM を挿入します。
