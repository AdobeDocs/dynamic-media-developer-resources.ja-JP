---
description: 返信画像のサイズの制限。 クライアントに返される返信画像の幅と高さの最大値。
seo-description: 返信画像のサイズの制限。 クライアントに返される返信画像の幅と高さの最大値。
seo-title: MaxPix
solution: Experience Manager
title: MaxPix
topic: Scene7 Image Serving - Image Rendering API
uuid: 22c5fac8-1e64-4917-8bb8-69a95ab549cb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# MaxPix{#maxpix}

返信画像のサイズの制限。 クライアントに返される返信画像の幅と高さの最大値。

要求によって幅または高さがより大きい応答画像が生じる場合、サーバーはエラーを返しま `attribute::MaxPix`す。

## プロパティ {#section-b175425b9e9f48e0b1a71640f6a9e936}

0より大きい2つの整数で、コンマで区切ります。 幅と高さ（ピクセル単位） また、返信画像のサイズに制限を `0,0` 設けずに許可するようにに設定することもできます。

## 初期設定 {#section-1003537434da432fb2af100ecdbf9d72}

定義されていな `default::MaxPix` い場合や空の場合に継承されます。

## 関連項目 {#section-7385697a1b86482bba19db894f7af95b}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
