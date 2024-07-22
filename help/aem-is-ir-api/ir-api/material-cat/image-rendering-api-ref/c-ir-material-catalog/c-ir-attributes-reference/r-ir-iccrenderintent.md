---
title: IccRenderIntent
description: カラー変換レンダリングの方法。 レンダリングインテントが「icc=」で指定されていない場合のカラー変換のデフォルトのレンダリングインテントを提供します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86cc907d-556c-40ec-a104-2f0dcf9ed1ce
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 3%

---

# IccRenderIntent{#iccrenderintent}

カラー変換レンダリングの方法。 レンダリングインテントが `icc=` で指定されていない場合に、カラー変換のデフォルトのレンダリングインテントを提供します。

## プロパティ {#section-0a38c60e1525426185616c42824aee2c}

列挙値。 知覚的な場合は 0、相対的な色域を維持する場合は 1、彩度の場合は 2、絶対的な色域を維持する場合は 3 に設定します。 カラープロファイルで定義されたデフォルトのレンダリングインテントを使用するには、空のままにするか、他の値に設定します。

## 初期設定 {#section-9301e3b7d0184ec5bf54a6eb73a6d3c1}

定義されていない場合は `default::IccRenderIntent` から継承。 空の場合は、「相対的な色域を保持」が適用されます。

## 関連項目 {#section-e77bcdfef6d2486ebd545631ccb40ebd}

[attribute::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127)、[attribute::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0)、[`icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)
