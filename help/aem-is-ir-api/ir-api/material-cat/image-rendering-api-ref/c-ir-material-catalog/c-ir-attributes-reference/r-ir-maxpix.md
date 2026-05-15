---
title: MaxPix
description: 返信画像サイズの制限。 クライアントに返される返信画像の最大幅と高さ。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48239519-7935-45e4-ae36-5e687a356cc1
TQID: 'https://experienceleague.adobe.com/pgrg9BCY7fJXGsoABNjMOwIhRxYzrmQpsDSyGd6GSCc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 103
ht-degree: 2%

---

# MaxPix{#maxpix}

返信画像サイズの制限。 クライアントに返される返信画像の最大幅と高さ。

リクエストで幅と高さが`attribute::MaxSize`より大きい返信画像が発生した場合、サーバーはエラーを返します。

## プロパティ {#section-390c1066b7a748aca3c0b45ad8bdcfb1}

0より大きい2つの整数値をコンマで区切ります。 幅と高さ（ピクセル単位）。 また、0,0に設定して、制限なしで任意の返信画像サイズを許可することもできます。

## 初期設定 {#section-45b38dc661854d11b97df5709f4f3434}

定義されていない場合や空の場合は、デフォルト : MaxPixから継承されます。

## 関連項目 {#section-09cddedde91f43b1ac5828f7e3327c6a}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec)、[hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
