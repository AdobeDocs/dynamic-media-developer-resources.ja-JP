---
description: デフォルトのビューサイズ。
solution: Experience Manager
title: DefaultPix
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 709fb2a1-1b9d-421e-9a65-5f5c74390ce3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 4%

---

# DefaultPix{#defaultpix}

デフォルトのビューサイズ。

サーバーによって、`wid=`、`hei=`または`scl=`を使用してビューサイズを明示的に指定しない場合、返信画像はこの幅と高さ以下に制限されます。

## プロパティ {#section-c3e658cf82c540d986b118f74f0fe1b2}

0以上の2つの整数で、コンマで区切ります。 幅と高さ（ピクセル単位）。 値を0に設定すると、値は制約なしに保たれます。

ネストされたリクエスト/埋め込みリクエストには適用されません。

## 初期設定 {#section-b7338b2bf5114fff83b0714a57b20639}

`default::DefaultPix`から継承されます（定義されていない場合または空の場合）。

## 関連項目 {#section-59088cd41da940e8ac0e74e2b049c6e9}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) 、 [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)、 [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)、 [catalog::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
