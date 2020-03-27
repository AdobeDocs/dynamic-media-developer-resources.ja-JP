---
description: 返信画像のサイズの制限。 クライアントに返される返信画像の幅と高さの最大値。
seo-description: 返信画像のサイズの制限。 クライアントに返される返信画像の幅と高さの最大値。
seo-title: MaxPix
solution: Experience Manager
title: MaxPix
topic: Scene7 Image Serving - Image Rendering API
uuid: 8fc5e032-cfbb-40b5-9c3a-a2ec1bc4c3e2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# MaxPix{#maxpix}

返信画像のサイズの制限。 クライアントに返される返信画像の幅と高さの最大値。

要求によって幅や高さがより大きい応答イメージが生じる場合、サーバはエラーを返しま `attribute::MaxSize`す。

## プロパティ {#section-390c1066b7a748aca3c0b45ad8bdcfb1}

0より大きい2つの整数で、コンマで区切ります。 幅と高さ（ピクセル単位） また、0,0に設定して、返信画像のサイズに制限を設けないようにします。

## 初期設定 {#section-45b38dc661854d11b97df5709f4f3434}

定義されていない場合、または空の場合は、default::MaxPixから継承されます。

## 関連項目 {#section-09cddedde91f43b1ac5828f7e3327c6a}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
