---
description: 画像サービングは、ISO-8859-1およびUTF-8エンコーディングの画像カタログをサポートします。
solution: Experience Manager
title: 文字エンコーディング
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: e6e50c2a-53d3-4776-a3f6-4a9d3407e562
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---

# 文字エンコーディング{#character-encoding}

画像サービングは、ISO-8859-1およびUTF-8エンコーディングの画像カタログをサポートします。

バイトオーダーマーク(BOM)は、各ファイルのエンコーディングを指定するために使用されます。 UTF-8の場合、BOMはバイトシーケンス`EF BB BF`です。 UTF-8エンコーディングは、各画像カタログファイルの最初にこの文字列が検出された場合に想定されます。 その他のバイトシーケンスは、ファイルがISO-8859-1標準にエンコードされていると解釈されます。

多くの現代アプリケーションは、UTF-8用に設定されている場合、BOMを自動的に挿入します。
