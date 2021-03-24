---
description: 返信画像のサイズ制限 クライアントに返すことのできる応答画像の幅と高さの最大値。
solution: Experience Manager
title: MaxPix
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '106'
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
