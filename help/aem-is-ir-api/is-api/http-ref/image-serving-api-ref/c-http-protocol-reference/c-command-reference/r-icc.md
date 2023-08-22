---
title: icc
description: 出力カラープロファイル.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8be7be8c-a23d-4a5b-93e4-44231155616b
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 3%

---

# icc{#icc}

出力カラープロファイル.

`icc= *`object`*[, *`renderIntent`*[, *`blackpointComp`*[, *`ディザ`*]]`

<table id="simpletable_AC20916999004CDCBBB9888B3A8FB0A7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> object</span> </span> </p></td> 
  <td class="stentry"> <p>ICC カラープロファイル。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 知覚的|相対的|彩度|絶対</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span></span> </p></td> 
  <td class="stentry"> <p>1 は有効に、0 は黒点補正を無効にします。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> ディザ</span></span> </p></td> 
  <td class="stentry"> <p>1 はディザリングを有効にし、0 はディザリングを無効にします。 </p></td> 
 </tr> 
</table>

*`object`* 作業プロファイルと異なる場合に画像の変換先となる出力カラースペースプロファイルを指定します。 *`profile`* は、有効な `icc::Name` 画像カタログまたはデフォルトカタログの ICC プロファイルマップ内で定義されるか、プロファイルファイルの相対パス ( 通常は [!DNL .icc] または [!DNL .icm] サフィックス ) です。 詳しくは、 [*`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) を参照してください。

>[!NOTE]
>
>*`object`* は、HTTP エンコードされている場合でも、「,」文字を含めることはできません。

*`renderIntent`* デフォルトのレンダリングインテントを上書きできます。

*`blackpointComp`* 出力プロファイルがこの機能をサポートしている場合、黒点補正を有効にします。

>[!NOTE]
>
>すべての色変換がサポートされているわけではありません *`renderIntent`* および *`blackpointComp`* 選択肢。 通常、これらの設定は、ICC 出力プロファイルがプリンタやモニタなどの出力デバイスを特徴付ける場合にのみ有効です。 また、一部の ICC 出力プロファイルは、一部の *`renderIntent`* 選択肢。

Note

*`dither`* ディザリング（実際にはエラー拡散）を有効にします。これにより、カラーバンディングアーティファクトを回避または軽減できます。

## プロパティ {#section-9fcd3e7bd1fd43c887b0f18a2f3c7259}

要求属性。 画像タイプがで指定されている場合、サーバーはエラーを返します。 `fmt=` 一致しない *`profile`*.

*`renderIntent`* および *`blackpointComp`* は、指定された ICC プロファイルと互換性がない場合は無視されます。 CMYK 出力デバイスプロファイルは、様々なレンダリング意図をサポートする可能性が高くなります。

## 初期設定 {#section-0b9fe2eb428447df8ae9948f11ab5aae}

カラーマネジメントが有効になっていて、 `icc=` が指定されていない場合、サーバーは出力プロファイル ( `attribute::IccProfile*`) が `fmt=`.

指定しない場合、 *`renderIntent`* は次から継承されます： `attribute::IccRenderIntent`, *`blackpointComp`* は次から継承されます： `attribute::IccBlackPointCompensation`、および *`dither`* は次から継承されます： `attribute::IccDither`.

## 関連項目 {#section-37f16b0c2c4b48f3a39dcde2a350f91e}

[attribute::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [attribute::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a), [object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0), [カラーマネジメント](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7), [ICC プロファイルマップリファレンス](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)
