---
description: カラー変換レンダリングインテント。 icc=でレンダリングインテントが指定されていない場合のカラー変換に対する初期設定のレンダリングインテントを指定します。
seo-description: カラー変換レンダリングインテント。 icc=でレンダリングインテントが指定されていない場合のカラー変換に対する初期設定のレンダリングインテントを指定します。
seo-title: IccRenderIntent
solution: Experience Manager
title: IccRenderIntent
topic: Scene7 Image Serving - Image Rendering API
uuid: a9648405-32c3-4762-bbb2-11e97d4f8374
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 3%

---


# IccRenderIntent{#iccrenderintent}

カラー変換レンダリングインテント。 icc=でレンダリングインテントが指定されていない場合のカラー変換に対する初期設定のレンダリングインテントを指定します。

## プロパティ {#section-0a38c60e1525426185616c42824aee2c}

列挙。 知覚的には0、相対的な色域を維持するには1、彩度には2、絶対的な色域を維持するには3に設定します。 空のままにするか、その他の値に設定すると、カラープロファイルで定義されている初期設定のレンダリングインテントが使用されます。

## 初期設定 {#section-9301e3b7d0184ec5bf54a6eb73a6d3c1}

`default::IccRenderIntent`から継承（定義されていない場合）。 空の場合は、「相対的な色域を保持」が適用されます。

## 関連項目 {#section-e77bcdfef6d2486ebd545631ccb40ebd}

[attribute::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127) ,  [attribute::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0),  [icc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)
