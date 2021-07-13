---
description: 返信画像のサイズ制限。 クライアントに返す応答画像の最大の幅と高さ。
solution: Experience Manager
title: MaxPix
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 0fd990cf-a54f-4574-8328-8988368d5875
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 3%

---

# MaxPix{#maxpix}

返信画像のサイズ制限。 クライアントに返す応答画像の最大の幅と高さ。

要求により、幅または高さが`attribute::MaxPix`より大きい返信画像が生成された場合、サーバーはエラーを返します。

## プロパティ {#section-b175425b9e9f48e0b1a71640f6a9e936}

0より大きい2つの整数で、コンマで区切ります。 幅と高さ（ピクセル単位）。 また、`0,0`に設定して、返信画像のサイズに制限を設けないようにすることもできます。

## 初期設定 {#section-1003537434da432fb2af100ecdbf9d72}

`default::MaxPix`から継承されます（定義されていない場合または空の場合）。

## 関連項目 {#section-7385697a1b86482bba19db894f7af95b}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) 、 [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
