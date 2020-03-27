---
description: 出力カラープロファイル.
seo-description: 出力カラープロファイル.
seo-title: icc
solution: Experience Manager
title: icc
topic: Scene7 Image Serving - Image Rendering API
uuid: cfbd18aa-cbba-4085-920d-1f54645d0f89
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# icc{#icc}

出力カラープロファイル.

`icc= *`objectrenderIntentblackpointCompdither`*[, *``*[, *``*[, *``*]]`

<table id="simpletable_AC20916999004CDCBBB9888B3A8FB0A7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 物 <span class="varname"> 体</span></span> </p></td> 
  <td class="stentry"> <p>ICCカラープロファイル。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> renderIntent <span class="varname"></span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> perceptical|relative|saturation|absolute</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> blackpointComp <span class="varname"></span></span> </p></td> 
  <td class="stentry"> <p>1を指定すると有効になり、0を指定するとブラックポイントの補正が無効になります。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> ディザ</span></span> </p></td> 
  <td class="stentry"> <p>1を指定するとディザが有効になり、0を指定するとディザが無効になります。 </p></td> 
 </tr> 
</table>

*`object`* は、作業プロファイルと異なる場合に画像を変換する出力カラースペースプロファイルを指定します。 *`profile`* は、画像カタログのICCプ `icc::Name` ロファイルマップまたは初期設定のカタログで定義された有効なパス、またはプロファイルファイルの相対パス(通常は、またはサフィックスを付 [!DNL .icc] けたパス [!DNL .icm] )である必要があります。 See [ *`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)for additional information.

>[!NOTE]
>
>*`object`* は、HTTPエンコードされている場合でも、「,」文字を含めることはできません。

*`renderIntent`* 初期設定のレンダリングインテントを上書きできます。

*`blackpointComp`* 出力プロファイルがこの機能をサポートしている場合、ブラックポイントの補正を有効にします。

>[!NOTE]
>
>すべての色変換が、選択肢をサポートしてい *`renderIntent`* るわけでは *`blackpointComp`* ありません。 通常、これらの設定は、ICC出力プロファイルがプリンターやモニターなどの出力デバイスの特性を示す場合にのみ適用されます。 また、一部のICC出力プロファイルでは、選択肢の一部がサポートされて *`renderIntent`* いません。

Note

*`dither`* ディザリング（実際にはエラー拡散）を有効にします。これにより、カラーバンディングのアーチファクトを回避または減少させることがあります。

## プロパティ {#section-9fcd3e7bd1fd43c887b0f18a2f3c7259}

リクエスト属性。 イメージタイプが指定されていて、一致しない場合、サーバは `fmt=` エラーを返しま *`profile`*&#x200B;す。

*`renderIntent`* とは、指 *`blackpointComp`* 定したICCプロファイルと互換性がない場合は無視されます。 CMYK出力デバイスプロファイルは、様々なレンダリングインテントをサポートする可能性が高くなります。

## 初期設定 {#section-0b9fe2eb428447df8ae9948f11ab5aae}

カラーマネジメントが有効で、指定さ `icc=` れていない場合、サーバは、で指定された画像タイプに一致する出力プロファイル( `attribute::IccProfile*`)に変換された画像を配信しま `fmt=`す。

指定しなかった場合、は *`renderIntent`* から継承され、はか `attribute::IccRenderIntent`ら継 *`blackpointComp`* 承され、はか `attribute::IccBlackPointCompensation`ら *`dither`* 継承されま `attribute::IccDither`す。は、から継承されます。

## 関連項目 {#section-37f16b0c2c4b48f3a39dcde2a350f91e}

[attribute::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) , [attribute::RenderProfileIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [, attribute::IccPoint Compensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)[:IccDitherDitherDitherDitherFmt=object, attribute, Color Management, ICC Profile, Profile Profileembed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)
