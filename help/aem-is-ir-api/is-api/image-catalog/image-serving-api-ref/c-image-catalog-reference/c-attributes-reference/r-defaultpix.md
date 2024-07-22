---
description: デフォルトの表示サイズ。
solution: Experience Manager
title: DefaultPix
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 709fb2a1-1b9d-421e-9a65-5f5c74390ce3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 3%

---

# DefaultPix{#defaultpix}

デフォルトの表示サイズ。

リクエストで `wid=`、`hei=`、`scl=` を使用して表示サイズを明示的に指定していない場合、サーバーによって、返信画像がこの幅と高さを超えないように制限されます。

## プロパティ {#section-c3e658cf82c540d986b118f74f0fe1b2}

コンマで区切られた 0 以上の 2 つの整数。 幅と高さ（ピクセル単位）。 一方または両方の値を 0 に設定すると、制限なしにすることができます。

ネストされたリクエストまたは埋め込まれたリクエストに対しては適用されません。

## 初期設定 {#section-b7338b2bf5114fff83b0714a57b20639}

定義されていない場合または空の場合は `default::DefaultPix` から継承します。

## 関連項目 {#section-59088cd41da940e8ac0e74e2b049c6e9}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [catalog::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
