---
description: 初期設定のサムネールサイズ サムネール要求(req=tmb)に対して、属性DefaultPixの代わりに使用されます。
solution: Experience Manager
title: DefaultThumbPix
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 3%

---


# DefaultThumbPix{#defaultthumbpix}

初期設定のサムネールサイズ サムネールリクエスト(req=tmb)の場合に、attribute::DefaultPixの代わりに使用されます。

サムネール要求(`req=tmb`)が`wid=`、`hei=`または`scl=`を使用して明示的に表示サイズを指定しないサイズを明示的に指定しない場合、応答画像はこの幅と高さ以下に制限されます。

## プロパティ {#section-650d9b1194fb4c47a03c6809e6b4af0e}

0以上の2つの整数で、カンマで区切ります。 幅と高さ（ピクセル単位） どちらかまたは両方の値を0に設定して、拘束を適用しないようにすることができます。

ネストされた/埋め込まれたリクエストには適用されません。

## 初期設定 {#section-2c4a4f14540449638822913513170ff1}

定義されていない場合や空の場合は`default::DefaultThumbPix`から継承されます。

## 関連項目 {#section-4ad00963ffa049fcb17ad63e6bbe7ac4}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
