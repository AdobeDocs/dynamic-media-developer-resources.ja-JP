---
title: IccProfileSrcCmyk
description: CMYK デフォルトの入力カラープロファイル。 カラープロファイルを埋め込まないCMYK マテリアル画像に使用するICC カラープロファイルの名前を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 09be34c8-facc-40c3-ba15-c48bd93b3be1
TQID: 'https://experienceleague.adobe.com/AX-NqS0F7TjgfLR2S8xyrJukDlB8-n-d17Bcn--AFrg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 2%

---

# IccProfileSrcCmyk{#iccprofilesrccmyk}

CMYK デフォルトの入力カラープロファイル。 カラープロファイルを埋め込まないCMYK マテリアル画像に使用するICC カラープロファイルの名前を指定します。

## プロパティ {#section-0cee77438d914c319ec876edb3490821}

テキスト文字列。 指定する場合は、この画像カタログまたはデフォルトカタログのICC プロファイルマップからの有効な`icc::Name`値、または`attribute::RootPath`に対するファイルパスである必要があります。 参照されるICC プロファイルは、CMYK プロファイルである必要があります。

## 初期設定 {#section-11f6239e0dd14827abf4a95c1b30161c}

定義されていない場合や空の場合は、`default::IccProfileSrcCmyk`から継承されます。 `attribute::IccProfileSrcCmyk`が有効なプロファイルに解決しない場合は、代わりに`attribute::IccProfileCmyk`が使用されます。

## 関連項目 {#section-88adddd70265459a9a5d2f50829a4ba7}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2)、[属性：:IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)、[属性：:IccProfileCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127)、[属性：:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
