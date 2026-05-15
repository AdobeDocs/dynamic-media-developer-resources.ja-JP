---
description: デフォルトのサムネールサイズ。 サムネール要求（req=tmb）の属性DefaultPixの代わりに使用されます。
solution: Experience Manager
title: DefaultThumbPix
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c1413da0-a68d-4345-928f-b532991966a8
TQID: 'https://experienceleague.adobe.com/GapTE3HrLMpk0vTGpJEihwZ45W6U3rZFnd9jYGcg9co'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 112
ht-degree: 2%

---

# DefaultThumbPix{#defaultthumbpix}

デフォルトのサムネールサイズ。 サムネールリクエストの場合は、属性：:DefaultPixの代わりに使用されます（req=tmb）。

サムネールリクエスト（`req=tmb`）でサイズが明示的に指定されていない場合、`wid=`、`hei=`、または`scl=`を使用してビューサイズを明示的に指定しない場合、サーバーは返信画像をこの幅および高さより大きくしないように制限します。

## プロパティ {#section-650d9b1194fb4c47a03c6809e6b4af0e}

0以上の2つの整数値をコンマで区切ります。 幅と高さ（ピクセル単位）。 どちらか一方または両方の値を0に設定して、制限を解除します。

ネストされたリクエストや埋め込まれたリクエストには適用されません。

## 初期設定 {#section-2c4a4f14540449638822913513170ff1}

定義されていない場合や空の場合は、`default::DefaultThumbPix`から継承されます。

## 関連項目 {#section-4ad00963ffa049fcb17ad63e6bbe7ac4}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47)、[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)、[scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)、[属性：:DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
