---
title: icc
description: 出力カラープロファイル。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8be7be8c-a23d-4a5b-93e4-44231155616b
TQID: 'https://experienceleague.adobe.com/Hg1FY5migettNtLHrXevywDf07HhOejo5Z05l8d4lRU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 281
ht-degree: 1%

---

# icc{#icc}

出力カラープロファイル。

`icc= *` オブジェクト `*[, *`renderIntent`*[, *`blackpointComp`*[, *`dither`*]]`

<table id="simpletable_AC20916999004CDCBBB9888B3A8FB0A7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> オブジェクト </span> </span> </p></td> 
  <td class="stentry"> <p>ICC カラープロファイル。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph">知覚的|相対|彩度|絶対</span>。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span></span> </p></td> 
  <td class="stentry"> <p>1を有効にする場合は0、ブラックポイントの補償を無効にする場合は0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> dither</span></span> </p></td> 
  <td class="stentry"> <p>ディザリングを有効にするには1、無効にするには0。 </p></td> 
 </tr> 
</table>

値&#x200B;*`object`*&#x200B;は、画像が作業用プロファイルと異なる場合に変換する出力色空間プロファイルを指定します。 値&#x200B;*`profile`*&#x200B;は、画像カタログまたはデフォルトカタログのICC プロファイルマップで定義された有効な`icc::Name`か、プロファイルファイルへの相対パス（通常は[!DNL .icc]または[!DNL .icm]接尾辞）である必要があります。 詳しくは、[*`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)を参照してください。

>[!NOTE]
>
>値&#x200B;*`object`*&#x200B;には、HTTP エンコードされた場合でも、「,」文字を含めることはできません。

値&#x200B;*`renderIntent`*&#x200B;を使用すると、デフォルトのレンダリングインテントを上書きできます。

出力プロファイルがこの機能をサポートしている場合、値&#x200B;*`blackpointComp`*&#x200B;はブラックポイント補正を有効にします。

>[!NOTE]
>
>すべてのカラーコンバージョンが&#x200B;*`renderIntent`*&#x200B;と&#x200B;*`blackpointComp`*&#x200B;のすべての選択肢をサポートしているわけではありません。 通常、これらの設定は、ICC出力プロファイルがプリンターやモニターなどの出力デバイスを特徴付ける場合にのみ適用されます。 また、一部のICC出力プロファイルは、すべての&#x200B;*`renderIntent`*&#x200B;の選択肢をサポートしていません。

Note

修飾子&#x200B;*`dither`*&#x200B;を使用すると、ディザ処理（実際にはエラー拡散）が可能になり、カラーバンディングアーティファクトを回避または削減できます。

## プロパティ {#section-9fcd3e7bd1fd43c887b0f18a2f3c7259}

リクエスト属性： 画像タイプが`fmt=`で指定されていて、*`profile`*&#x200B;と一致しない場合、サーバーはエラーを返します。

指定されたICC プロファイルと互換性がない場合、修飾子&#x200B;*`renderIntent`*&#x200B;と&#x200B;*`blackpointComp`*&#x200B;は無視されます。 CMYK出力デバイスプロファイルは、異なるレンダリングインテントをサポートする可能性が高くなります。

## 初期設定 {#section-0b9fe2eb428447df8ae9948f11ab5aae}

カラーマネジメントが有効で`icc=`が指定されていない場合、サーバーは、指定した画像タイプと`fmt=`が一致する出力プロファイル （`attribute::IccProfile*`）に変換された画像を配信します。

指定しない場合、*`renderIntent`*&#x200B;は`attribute::IccRenderIntent`から継承され、*`blackpointComp`*&#x200B;は`attribute::IccBlackPointCompensation`から継承され、*`dither`*&#x200B;は`attribute::IccDither`から継承されます。

## 関連項目 {#section-37f16b0c2c4b48f3a39dcde2a350f91e}

[属性：:IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)、[属性：:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)、[属性：:IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f)、[属性：:IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b)、[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)、[ オブジェクト ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)、[ カラーマネジメント ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)、[ICC プロファイル参照](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)、[iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)
