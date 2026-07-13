---
title: DefaultPix
description: デフォルトのレンダリング画像サイズ。 リクエストでwid=またはhei=を使用してビューサイズを明示的に指定しない場合、サーバーは返信画像をこの幅と高さより大きくしないように制限します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d60f2b8c-5213-42ad-8ec9-7e7797d74e09
TQID: 'https://experienceleague.adobe.com/n0m-j--YSFkdFmNOuJhRi3az-tARnc-N3sRmgkSJryE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 2%

---

# DefaultPix{#defaultpix}

デフォルトのレンダリング画像サイズ。 リクエストでwid=またはhei=を使用してビューサイズを明示的に指定しない場合、サーバーは返信画像をこの幅と高さより大きくしないように制限します。

## プロパティ {#section-9dc5474fc75842308796ab6440b29611}

0以上の2つの整数値をコンマで区切ります。 幅と高さ（ピクセル単位）。 どちらか一方または両方の値を0に設定して、制限を解除します。

ネストされたリクエストや埋め込まれたリクエストには適用されません。

## 初期設定 {#section-1935781c561e4679aa87a5bcced8df90}

定義されていない場合や空の場合は、`default::DefaultPix`から継承されます。

## 関連項目 {#section-d28f18d29ef14692b8706ca08e754f54}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec)、[hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)、[属性：:MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)

