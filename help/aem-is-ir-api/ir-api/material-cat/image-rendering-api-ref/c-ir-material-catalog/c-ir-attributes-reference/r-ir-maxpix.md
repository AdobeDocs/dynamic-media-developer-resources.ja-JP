---
title: MaxPix
description: 返信画像のサイズ制限。 クライアントに返す返信画像の最大の幅と高さ。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48239519-7935-45e4-ae36-5e687a356cc1
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# MaxPix{#maxpix}

返信画像のサイズ制限。 クライアントに返す返信画像の最大の幅と高さ。

要求により、幅や高さが以下の値を超える返信画像が生成された場合、サーバーはエラーを返します `attribute::MaxSize`.

## プロパティ {#section-390c1066b7a748aca3c0b45ad8bdcfb1}

0 より大きい 2 つの整数で、コンマで区切ります。 幅と高さ（ピクセル単位）。 また、0,0 に設定すると、返信画像のサイズに制限がなく許可されます。

## 初期設定 {#section-45b38dc661854d11b97df5709f4f3434}

定義されていない場合や空の場合は、default::MaxPix から継承されます。

## 関連項目 {#section-09cddedde91f43b1ac5828f7e3327c6a}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
