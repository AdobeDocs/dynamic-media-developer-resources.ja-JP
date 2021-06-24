---
description: 出力カラープロファイル.
solution: Experience Manager
title: icc
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 8be7be8c-a23d-4a5b-93e4-44231155616b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 4%

---

# icc{#icc}

出力カラープロファイル.

`icc= *``*[, *``*[, *``*[, *`objectrenderIntentblackpointCompdither`*]]`

<table id="simpletable_AC20916999004CDCBBB9888B3A8FB0A7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> object</span> </span> </p></td> 
  <td class="stentry"> <p>ICCカラープロファイル。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 知覚的|相対|彩度|絶対</span>。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span></span> </p></td> 
  <td class="stentry"> <p>1は有効に、0は黒点補正を無効にします。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> ディザ</span></span> </p></td> 
  <td class="stentry"> <p>1はディザリングを有効にし、0はディザリングを無効にします。 </p></td> 
 </tr> 
</table>

*`object`* は、作業プロファイルと異なる場合に画像の変換先となる出力カラースペースプロファイルを指定します。*`profile`* は、画像カタログまたはデ `icc::Name` フォルトカタログのICCプロファイルマップで定義されている有効なパス、またはプロファイルファイルの相対パス（通常は、またはサフィックスを持つ） [!DNL .icc] である必 [!DNL .icm] 要があります。詳しくは、 [ *`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)を参照してください。

>[!NOTE]
>
>*`object`* は、HTTPエンコードされている場合でも、「,」文字を含めることはできません。

*`renderIntent`* デフォルトのレンダリングインテントを上書きできます。

*`blackpointComp`* 出力プロファイルがこの機能をサポートしている場合、ブラックポイント補正を有効にします。

>[!NOTE]
>
>すべての&#x200B;*`renderIntent`*&#x200B;と&#x200B;*`blackpointComp`*&#x200B;の選択肢がカラー変換でサポートされているわけではありません。 通常、これらの設定は、ICC出力プロファイルがプリンターやモニターなどの出力デバイスを特徴付ける場合にのみ有効です。 また、一部のICC出力プロファイルは&#x200B;*`renderIntent`*&#x200B;の選択肢をサポートしていません。

Note

*`dither`* ディザリング（実際にはエラー拡散）を有効にし、カラーバンディングアーティファクトを回避または減らす可能性があります。

## プロパティ {#section-9fcd3e7bd1fd43c887b0f18a2f3c7259}

リクエスト属性。 *`profile`*&#x200B;と一致しないイメージタイプが`fmt=`で指定されている場合、サーバーはエラーを返します。

*`renderIntent`* および *`blackpointComp`* は、指定されたICCプロファイルと互換性がない場合は無視されます。CMYK出力デバイスプロファイルは、様々なレンダリング意図をサポートする可能性が高くなります。

## 初期設定 {#section-0b9fe2eb428447df8ae9948f11ab5aae}

カラーマネジメントが有効で`icc=`が指定されていない場合、サーバーは`fmt=`で指定された画像タイプに一致する出力プロファイル(`attribute::IccProfile*`)に変換された画像を配信します。

指定しなかった場合、*`renderIntent`*&#x200B;は`attribute::IccRenderIntent`から継承され、*`blackpointComp`*&#x200B;は`attribute::IccBlackPointCompensation`から継承され、*`dither`*&#x200B;は`attribute::IccDither`から継承されます。

## 関連項目 {#section-37f16b0c2c4b48f3a39dcde2a350f91e}

[attribute::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) 、 [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)、 [attribute::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f)、 [attribute::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b)、 [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)、 [object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)、 [カラーマネジメント](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)、 [ICCプロファイルマップリファレンス](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)、 [Iccembed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)
