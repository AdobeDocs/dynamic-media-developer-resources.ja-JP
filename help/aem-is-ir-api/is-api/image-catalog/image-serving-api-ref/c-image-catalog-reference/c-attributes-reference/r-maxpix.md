---
description: 返信画像のサイズ制限。 クライアントに返される返信画像の最大の幅と高さ。
solution: Experience Manager
title: MaxPix
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0fd990cf-a54f-4574-8328-8988368d5875
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 3%

---

# MaxPix{#maxpix}

返信画像のサイズ制限。 クライアントに返される返信画像の最大の幅と高さ。

リクエストによって返信画像の幅または高さが `attribute::MaxPix` を超える場合、サーバーはエラーを返します。

## プロパティ {#section-b175425b9e9f48e0b1a71640f6a9e936}

0 より大きい 2 つの整数。コンマで区切ります。 幅と高さ（ピクセル単位）。 また、を `0,0` に設定して、制限のない返信画像のサイズを許可することもできます。

## 初期設定 {#section-1003537434da432fb2af100ecdbf9d72}

定義されていない場合または空の場合は `default::MaxPix` から継承します。

## 関連項目 {#section-7385697a1b86482bba19db894f7af95b}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
