---
title: TiffEncoding
description: TIFFのエンコーディングフォーマット： TIFF イメージの圧縮形式を指定します（実際にはfmt= コマンドの3番目の値のデフォルト）。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6a6fa8f5-4497-438d-914c-3f6d4c08ef09
TQID: 'https://experienceleague.adobe.com/lSR8V09ooHaKYbD-GFAiuK-QcRJBKkXkVMTKy7Oj2e0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 71
ht-degree: 4%

---

# TiffEncoding{#tiffencoding}

TIFFのエンコーディングフォーマット： TIFF イメージの圧縮形式を指定します（実際には、`fmt=` コマンドの3番目の値のデフォルト）。

圧縮なしの場合は`0`、LZWの場合は`1`、デフレート（ZIP）の場合は`2`、JPEG圧縮の場合は`3`に設定します。

## プロパティ {#section-469f5a1225464542866f5353edd92db3}

列挙：

## 初期設定 {#section-a3c5152a9f464e4987ed7c05d35b1169}

定義されていない場合や空の場合は、`default::TiffEncoding`から継承されます。

## 関連項目 {#section-1601425e5ac3486da4df8e7fa55981b2}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)
