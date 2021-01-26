---
description: 出力カラープロファイル
seo-description: 出力カラープロファイル
seo-title: icc
solution: Experience Manager
title: icc
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 95a05fe5-d6b3-4118-aab4-4664ccee2850
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 1%

---


# icc{#icc}

出力カラープロファイル

icc= *`profile`*[, *`renderIntent`*[,*`blackpointComp`*]]

<table id="simpletable_DF1914FD351E4F2BA61372A52F0CFFBF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> プロファイル</span></span> </p></td> 
  <td class="stentry"> <p>ICCカラープロファイル </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent  </span> </span> </p></td> 
  <td class="stentry"> <p>知覚の |相対 |彩度 |絶対 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span> </span> </p></td> 
  <td class="stentry"> <p>1を指定すると有効になり、0を指定するとブラックポイントの補正が無効になります。 </p></td> 
 </tr> 
</table>

*`profile`* は、作業プロファイルと異なる場合にレンダリングイメージを変換する出力カラースペースプロファイルを指定します。*`profile`* は、画像カタログまたは初期設定のカタログのICCプロファイルマップで `icc::Name` 定義されている有効なパスか、プロファイルファイルの相対パス(通常は [!DNL .icc]、 [!DNL .icm] サフィックスを持つ)のいずれかにする必要があります。

>[!NOTE]
>
>*`profile`* は、HTTPエンコードされている場合でも、「,」文字を含めることはできません。

*`renderIntent`* 初期設定のレンダリングインテントを上書きできます。

*`blackpointComp`* 出力プロファイルがこの機能をサポートしている場合、ブラックポイント補正を有効にします。

>[!NOTE]
>
>すべての&#x200B;*`renderIntent`*&#x200B;と&#x200B;*`blackpointComp`*&#x200B;の選択肢をサポートしていない色変換もあります。 通常、これらの設定は、ICC出力プロファイルがプリンタやモニタなどの出力デバイスの特性を示す場合にのみ適用されます。 また、一部のICC出力プロファイルは、*`renderIntent`*&#x200B;の選択肢の一部をサポートしていません。

## プロパティ {#section-b4042623a8ea40248c11b2153e5906b1}

リクエスト内の任意の場所で発生する可能性があります。 `fmt=`で指定されたイメージタイプが&#x200B;*`profile`*&#x200B;と一致しない場合は、エラーが返されます。

*`renderIntent`* および *`blackpointComp`* は、指定したICCプロファイルと互換性がない場合は無視されます。

CMYK出力デバイスプロファイルでは、様々なレンダリング意図がサポートされる可能性が高くなります。

## 初期設定 {#section-bbd3206fdcac4dc48a08fc9eba14fc90}

カラーマネジメントが有効で`icc=`が指定されていない場合、サーバは`fmt=`で指定された画像の種類に合わせて出力プロファイル(`attribute::IccProfile*`)に変換された画像を配信します。

指定しなかった場合、*`renderIntent`*&#x200B;は`attribute::IccRenderIntent`から継承され、*`blackpointComp`*&#x200B;は`attribute::IccBlackPointCompensation`から継承されます。

## 関連項目 {#section-37ef83149fd74345956a98f633cc0294}

[Color Management](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-color-management.md#concept-7bac7c2c41be42c1b301eae80abe6b8d),  [attribute::IccProfile](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127),  [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f), iccEmbed= [, fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c) [](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40) [, *attribute:Icc Render IntentIntent:IccRender IntentAttribute:BlackPoint Compensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0)
