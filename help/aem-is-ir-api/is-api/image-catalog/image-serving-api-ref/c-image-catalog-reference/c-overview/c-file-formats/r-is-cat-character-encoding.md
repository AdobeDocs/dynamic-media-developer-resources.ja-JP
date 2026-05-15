---
description: 画像サービングは、ISO-8859-1およびUTF-8 エンコーディングを使用した画像カタログをサポートしています。
solution: Experience Manager
title: 文字エンコーディング
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e6e50c2a-53d3-4776-a3f6-4a9d3407e562
TQID: 'https://experienceleague.adobe.com/tsIJu-zCT-NlV6SD1I1pPYQ0DfqNcu9jSCBVXCcQ9tE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 104
ht-degree: 0%

---

# 文字エンコーディング{#character-encoding}

画像サービングは、ISO-8859-1およびUTF-8 エンコーディングを使用した画像カタログをサポートしています。

バイトオーダーマーク（BOM）を使用して、各ファイルのエンコーディングを指定します。 UTF-8の場合、BOMはバイト シーケンス `EF BB BF`です。 UTF-8 エンコーディングは、この文字シーケンスが各画像カタログファイルの先頭で検出された場合に想定されます。 他のバイト列では、ファイルはISO-8859-1規格にエンコードされていると解釈されます。

UTF-8用に設定されている多くの現代的なアプリケーションでは、BOMが自動的に挿入されます。
