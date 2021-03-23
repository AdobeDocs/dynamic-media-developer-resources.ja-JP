---
description: デフォルトの表示サイズ
seo-description: デフォルトの表示サイズ
seo-title: DefaultPix
solution: Experience Manager
title: DefaultPix
uuid: f5d2e4f7-f9c5-40a5-8a64-67241fcb0242
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 4%

---


# DefaultPix{#defaultpix}

デフォルトの表示サイズ

リクエストで`wid=`、`hei=`または`scl=`を使用して明示的に表示サイズを指定しない場合、応答画像はこの幅と高さ以下に制限されます。

## プロパティ {#section-c3e658cf82c540d986b118f74f0fe1b2}

0以上の2つの整数で、カンマで区切ります。 幅と高さ（ピクセル単位） どちらかまたは両方の値を0に設定して、拘束を適用しないようにすることができます。

ネストされた/埋め込まれたリクエストには適用されません。

## 初期設定 {#section-b7338b2bf5114fff83b0714a57b20639}

定義されていない場合や空の場合は`default::DefaultPix`から継承されます。

## 関連項目 {#section-59088cd41da940e8ac0e74e2b049c6e9}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [catalog::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
