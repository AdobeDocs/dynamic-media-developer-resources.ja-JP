---
description: デフォルトのビューサイズ。
solution: Experience Manager
title: DefaultPix
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 709fb2a1-1b9d-421e-9a65-5f5c74390ce3
TQID: 'https://experienceleague.adobe.com/R8zszzJJqviiIiIBt4GHGUmg5cX1yDxuhT6zoHllQKw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 86
ht-degree: 3%

---

# DefaultPix{#defaultpix}

デフォルトのビューサイズ。

リクエストで`wid=`、`hei=`、または`scl=`を使用してビューサイズを明示的に指定しない場合、サーバーは返信画像をこの幅および高さより大きくするように制限します。

## プロパティ {#section-c3e658cf82c540d986b118f74f0fe1b2}

0以上の2つの整数値をコンマで区切ります。 幅と高さ（ピクセル単位）。 どちらか一方または両方の値を0に設定して、制限を解除します。

ネストされたリクエストや埋め込まれたリクエストには適用されません。

## 初期設定 {#section-b7338b2bf5114fff83b0714a57b20639}

定義されていない場合や空の場合は、`default::DefaultPix`から継承されます。

## 関連項目 {#section-59088cd41da940e8ac0e74e2b049c6e9}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47)、[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)、[scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)、[ カタログ：:MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
