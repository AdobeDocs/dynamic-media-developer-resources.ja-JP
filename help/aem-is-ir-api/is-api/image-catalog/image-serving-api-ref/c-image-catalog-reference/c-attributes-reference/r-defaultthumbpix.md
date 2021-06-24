---
description: デフォルトのサムネールサイズ。 サムネール要求(req=tmb)の属性DefaultPixの代わりに使用されます。
solution: Experience Manager
title: DefaultThumbPix
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: c1413da0-a68d-4345-928f-b532991966a8
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 3%

---

# DefaultThumbPix{#defaultthumbpix}

デフォルトのサムネールサイズ。 サムネールリクエスト(req=tmb)にattribute::DefaultPixの代わりに使用されます。

サーバーによって、返信画像がこの幅と高さ以下に制限されます。サムネール要求(`req=tmb`)で`wid=`、`hei=`または`scl=`を使用して表示サイズを明示的に指定しない場合に限られます。

## プロパティ {#section-650d9b1194fb4c47a03c6809e6b4af0e}

0以上の2つの整数で、コンマで区切ります。 幅と高さ（ピクセル単位）。 値を0に設定すると、値は制約なしに保たれます。

ネストされたリクエスト/埋め込みリクエストには適用されません。

## 初期設定 {#section-2c4a4f14540449638822913513170ff1}

`default::DefaultThumbPix`から継承されます（定義されていない場合または空の場合）。

## 関連項目 {#section-4ad00963ffa049fcb17ad63e6bbe7ac4}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) 、 [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)、 [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)、 [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
