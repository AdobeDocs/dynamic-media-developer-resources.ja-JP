---
description: 画像のレンダリングは、ISO-8859-1およびUTF-8エンコーディングのマテリアルカタログをサポートします。
solution: Experience Manager
title: 文字エンコーディング
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: ee7b33fd-7607-4bff-867b-6e7a837a9ed4
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---

# 文字エンコーディング{#character-encoding}

画像のレンダリングは、ISO-8859-1およびUTF-8エンコーディングのマテリアルカタログをサポートします。

バイトオーダーマーク(BOM)は、各ファイルのエンコーディングを指定するために使用されます。 UTF-8の場合、BOMはバイトシーケンス`EF BB BF`です。 UTF-8エンコーディングは、各マテリアルカタログファイルの最初にこの文字列が検出された場合に想定されます。 その他のバイト列は、そのファイルがISO-8859-1標準にエンコードされたものと解釈されます。

多くの現代アプリケーションは、UTF-8用に設定されている場合、BOMを自動的に挿入します。
