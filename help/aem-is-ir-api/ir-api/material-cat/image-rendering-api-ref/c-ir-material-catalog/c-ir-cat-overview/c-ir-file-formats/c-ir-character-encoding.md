---
title: 文字エンコーディング
description: 画像レンダリングは、ISO-8859-1およびUTF-8 エンコーディングを使用したマテリアルカタログをサポートしています。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ee7b33fd-7607-4bff-867b-6e7a837a9ed4
TQID: 'https://experienceleague.adobe.com/1ITLimvCUD8hrdfeyyod6nE0sMmfIJ3ySx5HCFa2ZQk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 104
ht-degree: 0%

---

# 文字エンコーディング{#character-encoding}

画像レンダリングは、ISO-8859-1およびUTF-8 エンコーディングを使用したマテリアルカタログをサポートしています。

バイトオーダーマーク（BOM）を使用して、各ファイルのエンコーディングを指定します。 UTF-8の場合、BOMはバイト シーケンス `EF BB BF`です。 UTF-8 エンコーディングは、この文字シーケンスが各マテリアルカタログファイルの最初の部分で検出された場合に想定されます。 その他のバイトシーケンスでは、ファイルがISO-8859-1規格にエンコードされていると解釈されます。

多くの現代的なアプリケーションは、UTF-8用に設定されている場合、BOMを自動的に挿入します。
