---
title: icc
description: 出力カラープロファイル。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8be7be8c-a23d-4a5b-93e4-44231155616b
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 1%

---

# icc{#icc}

出力カラープロファイル。

`icc= *`object`*[, *`renderIntent`*[, *`blackpointComp`*[, *`dither`*]]`

<table id="simpletable_AC20916999004CDCBBB9888B3A8FB0A7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> オブジェクト </span> </span> </p></td> 
  <td class="stentry"> <p>ICC カラープロファイル。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 知覚的|相対的|彩度|絶対的 </span>。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span></span> </p></td> 
  <td class="stentry"> <p>1 を有効にするには、0 を指定するとブラックポイント補正が無効になります。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> ディザ </span></span> </p></td> 
  <td class="stentry"> <p>1：有効、0：ディザリング無効。 </p></td> 
 </tr> 
</table>

値 *`object`* は、画像が作業プロファイルと異なる場合に変換される出力カラースペースプロファイルを指定します。 値 *`profile`* は、画像カタログの ICC プロファイルマップまたはデフォルトカタログで定義された有効な `icc::Name`、またはプロファイルファイルへの相対パス（通常は [!DNL .icc] または [!DNL .icm] サフィックスを含む）にする必要があります。 詳細は、[*`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) を参照してください。

>[!NOTE]
>
>HTTP エンコードされた場合でも、値 *`object`* に「,」文字を含めることはできません。

値 *`renderIntent`* を使用すると、デフォルトのレンダリングインテントを上書きできます。

出力プロファイル *`blackpointComp`* この機能をサポートしている場合、値はブラックポイント補正を有効にします。

>[!NOTE]
>
>すべてのカラー変換ですべての *`renderIntent`* および *`blackpointComp`* の選択がサポートされているわけではありません。 通常、これらの設定は、ICC 出力プロファイルがプリンターやモニターなどの出力デバイスを特徴付ける場合にのみ適用されます。 また、一部の ICC 出力プロファイルは、*`renderIntent`* の選択肢の一部をサポートしていません。

Note

この修飾子 *`dither`* は、ディザリング（実際にはエラーディフュージョン）を有効にするので、カラーバンディングアーティファクトを回避または削減できます。

## プロパティ {#section-9fcd3e7bd1fd43c887b0f18a2f3c7259}

リクエスト属性。 一致しない `fmt=` で画像タイプが指定されている場合、サーバーはエラーを返 *`profile`* ます。

修飾子 *`renderIntent`* および *`blackpointComp`* は、指定された ICC プロファイルに適合しない場合、無視されます。 CMYK 出力デバイスプロファイルは、異なるレンダリングインテントをサポートする可能性が高くなります。

## 初期設定 {#section-0b9fe2eb428447df8ae9948f11ab5aae}

カラーマネジメントが有効になっていて、`icc=` が指定されていない場合、サーバーは `attribute::IccProfile*` で指定された画像タイプに一致する画像を出力プロファイル（`fmt=`）に変換して配信します。

指定しない場合、*`renderIntent`* は `attribute::IccRenderIntent` から、*`blackpointComp`* は `attribute::IccBlackPointCompensation` から、*`dither`* は `attribute::IccDither` から継承されます。

## 関連項目 {#section-37f16b0c2c4b48f3a39dcde2a350f91e}

[attribute::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)、[attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)、[attribute::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f)、[attribute::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b)、[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)、[object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)、[&#x200B; カラーマネジメント &#x200B;](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)、[ICC プロファイルマップ参照 &#x200B;](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)、[iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)
