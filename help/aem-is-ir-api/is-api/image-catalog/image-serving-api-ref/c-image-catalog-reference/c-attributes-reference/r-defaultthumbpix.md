---
description: 初期設定のサムネールサイズ サムネールリクエスト(req=tmb)の属性DefaultPixの代わりに使用されます。
seo-description: 初期設定のサムネールサイズ サムネールリクエスト(req=tmb)の属性DefaultPixの代わりに使用されます。
seo-title: DefaultThumbPix
solution: Experience Manager
title: DefaultThumbPix
topic: Scene7 Image Serving - Image Rendering API
uuid: 7b310aab-6d38-45f3-a3e7-b074a8e7a795
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# DefaultThumbPix{#defaultthumbpix}

初期設定のサムネールサイズ サムネールリクエスト(req=tmb)の場合、attribute::DefaultPixの代わりに使用されます。

サムネール要求( `req=tmb`)でサイズが明示的に指定されていない場合、、 、またはを使用してビューサイズが明示的に指定されていないと、応答画像はこの幅と高さ以下に制 `wid=`限さ `hei=`れま `scl=`す。

## プロパティ {#section-650d9b1194fb4c47a03c6809e6b4af0e}

0以上の2つの整数で、コンマで区切ります。 幅と高さ（ピクセル単位） どちらかまたは両方の値を0に設定して、制約を受けないようにすることができます。

ネストされた/埋め込まれたリクエストには適用されません。

## 初期設定 {#section-2c4a4f14540449638822913513170ff1}

定義されていな `default::DefaultThumbPix` い場合や空の場合に継承されます。

## 関連項目 {#section-4ad00963ffa049fcb17ad63e6bbe7ac4}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
