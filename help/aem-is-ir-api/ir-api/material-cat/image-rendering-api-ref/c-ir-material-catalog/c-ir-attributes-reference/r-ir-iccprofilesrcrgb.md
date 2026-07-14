---
title: IccProfileSrcRgb
description: RGBのデフォルト入力カラープロファイル。 カラープロファイルを埋め込まないRGB マテリアル画像や周辺光量補正に使用するICC カラープロファイルの名前を指定します。 また、bgc=やcolor=など、様々な画像レンダリングコマンドで指定されたRGBのカラー値にも対応しています。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1c90c77c-79b7-41aa-9269-b48d966ba362
TQID: 'https://experienceleague.adobe.com/P38eqZb2sT2vSm0qJDljwW319qWiCttn3V3CPwC-IWg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 159
ht-degree: 1%

---

# IccProfileSrcRgb{#iccprofilesrcrgb}

RGBのデフォルト入力カラープロファイル。 カラープロファイルを埋め込まないRGB マテリアル画像や周辺光量補正に使用するICC カラープロファイルの名前を指定します。 また、`bgc=`や`color=`など、様々な画像レンダリングコマンドで指定されたRGB カラー値も対象です。

## プロパティ {#section-c22966bba03e43c08e9d3fb91bfdd465}

テキスト文字列。 指定する場合は、この画像カタログまたはデフォルトカタログのICC プロファイルマップからの有効な`icc::Name`値、または`attribute::RootPath`に対するファイルパスである必要があります。 参照されるICC プロファイルは、RGB プロファイルである必要があります。

## 初期設定 {#section-0171cd6680284bfa9844b9cc3644ca61}

定義されていない場合や空の場合は、`default::IccProfileSrcRgb`から継承されます。 `attribute::IccProfileSrcRgb`が有効なプロファイルに解決しない場合は、代わりに`attribute::IccProfileRgb`が使用されます。

## 関連項目 {#section-1ba91666830f4c209c39260ea29f938e}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2)、[属性：:IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)、[属性：:IccProfileRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30)、[属性：:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)

