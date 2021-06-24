---
description: 返信画像のサイズ制限。 クライアントに返す応答画像の最大の幅と高さ。
solution: Experience Manager
title: MaxPix
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 48239519-7935-45e4-ae36-5e687a356cc1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 3%

---

# MaxPix{#maxpix}

返信画像のサイズ制限。 クライアントに返す応答画像の最大の幅と高さ。

要求によって、幅や高さが`attribute::MaxSize`より大きい返信画像が生成された場合、サーバはエラーを返します。

## プロパティ {#section-390c1066b7a748aca3c0b45ad8bdcfb1}

0より大きい2つの整数で、コンマで区切ります。 幅と高さ（ピクセル単位）。 また、0,0に設定して、返信画像のサイズに制限を設けないようにすることもできます。

## 初期設定 {#section-45b38dc661854d11b97df5709f4f3434}

定義されていない場合や空の場合は、default::MaxPixから継承されます。

## 関連項目 {#section-09cddedde91f43b1ac5828f7e3327c6a}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) 、 [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
