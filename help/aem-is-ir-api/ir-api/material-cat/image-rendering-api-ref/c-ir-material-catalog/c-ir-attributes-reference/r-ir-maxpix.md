---
description: 返信画像のサイズ制限 クライアントに返すことのできる応答画像の幅と高さの最大値。
solution: Experience Manager
title: MaxPix
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---


# MaxPix{#maxpix}

返信画像のサイズ制限 クライアントに返すことのできる応答画像の幅と高さの最大値。

リクエストによって、幅または高さが`attribute::MaxSize`より大きい応答画像が生成される場合、サーバはエラーを返します。

## プロパティ {#section-390c1066b7a748aca3c0b45ad8bdcfb1}

0より大きい2つの整数で、カンマで区切ります。 幅と高さ（ピクセル単位） また、0,0に設定して、返信画像のサイズに制限を設けないようにすることもできます。

## 初期設定 {#section-45b38dc661854d11b97df5709f4f3434}

定義されていない場合、または空の場合は、default::MaxPixから継承されます。

## 関連項目 {#section-09cddedde91f43b1ac5828f7e3327c6a}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) 、 [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
