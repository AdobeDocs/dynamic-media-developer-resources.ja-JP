---
title: IccRenderIntent
description: カラー変換レンダリングの方法。 icc=でレンダリングインテントが指定されていない場合の、カラー変換のデフォルトのレンダリング方法を提供します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86cc907d-556c-40ec-a104-2f0dcf9ed1ce
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# IccRenderIntent{#iccrenderintent}

カラー変換レンダリングの方法。 レンダリング方法が指定されていない場合に、色変換の既定のレンダリング方法を指定します。 `icc=`.

## プロパティ {#section-0a38c60e1525426185616c42824aee2c}

列挙。 知覚的には 0、相対的な色域を維持するには 1、彩度には 2、絶対的な色域を維持するには 3 に設定します。 空のままにするか、他の値に設定すると、カラープロファイルで定義されたデフォルトのレンダリング方法が使用されます。

## 初期設定 {#section-9301e3b7d0184ec5bf54a6eb73a6d3c1}

継承元 `default::IccRenderIntent`（定義されていない場合） 空の場合は、「相対的な色域を維持」が適用されます。

## 関連項目 {#section-e77bcdfef6d2486ebd545631ccb40ebd}

[attribute::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127) , [attribute::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0), [icc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)
