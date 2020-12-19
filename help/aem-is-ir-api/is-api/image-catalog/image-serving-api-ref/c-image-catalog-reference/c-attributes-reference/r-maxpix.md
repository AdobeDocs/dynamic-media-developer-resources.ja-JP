---
description: 返信画像のサイズ制限 クライアントに返すことのできる応答画像の幅と高さの最大値。
seo-description: 返信画像のサイズ制限 クライアントに返すことのできる応答画像の幅と高さの最大値。
seo-title: MaxPix
solution: Experience Manager
title: MaxPix
topic: Scene7 Image Serving - Image Rendering API
uuid: 22c5fac8-1e64-4917-8bb8-69a95ab549cb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 3%

---


# MaxPix{#maxpix}

返信画像のサイズ制限 クライアントに返すことのできる応答画像の幅と高さの最大値。

要求によって`attribute::MaxPix`より大きい幅または高さの応答画像が生じる場合、サーバはエラーを返します。

## プロパティ {#section-b175425b9e9f48e0b1a71640f6a9e936}

0より大きい2つの整数で、カンマで区切ります。 幅と高さ（ピクセル単位） また、`0,0`に設定して、返信画像のサイズに制限を設けないようにすることもできます。

## 初期設定 {#section-1003537434da432fb2af100ecdbf9d72}

定義されていない場合や空の場合は`default::MaxPix`から継承されます。

## 関連項目 {#section-7385697a1b86482bba19db894f7af95b}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) 、 [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
