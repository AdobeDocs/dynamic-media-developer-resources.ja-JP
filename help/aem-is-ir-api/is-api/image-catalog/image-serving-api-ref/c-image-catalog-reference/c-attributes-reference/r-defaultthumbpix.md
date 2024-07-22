---
description: デフォルトのサムネールサイズ。 サムネール要求（req=tmb）で DefaultPix 属性の代わりに使用されます。
solution: Experience Manager
title: DefaultThumbPix
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c1413da0-a68d-4345-928f-b532991966a8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 2%

---

# DefaultThumbPix{#defaultthumbpix}

デフォルトのサムネールサイズ。 サムネール要求（req=tmb）で attribute::DefaultPix の代わりに使用されます。

サムネールリクエスト（`req=tmb`）で、サイズが `wid=`、`hei=`、`scl=` を使用して表示サイズを明示的に指定していない場合、サーバーによって、返信画像がこの幅と高さを超えないように制限されます。

## プロパティ {#section-650d9b1194fb4c47a03c6809e6b4af0e}

コンマで区切られた 0 以上の 2 つの整数。 幅と高さ（ピクセル単位）。 一方または両方の値を 0 に設定すると、制限なしにすることができます。

ネストされたリクエストまたは埋め込まれたリクエストに対しては適用されません。

## 初期設定 {#section-2c4a4f14540449638822913513170ff1}

定義されていない場合または空の場合は `default::DefaultThumbPix` から継承します。

## 関連項目 {#section-4ad00963ffa049fcb17ad63e6bbe7ac4}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
