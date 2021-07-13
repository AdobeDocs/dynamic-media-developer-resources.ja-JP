---
description: 出力カラープロファイル
solution: Experience Manager
title: icc
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 39b25f7c-ed3c-4132-8241-e7f3aab07b00
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 1%

---

# icc{#icc}

出力カラープロファイル

icc= *`profile`*[, *`renderIntent`*[,*`blackpointComp`*]]

<table id="simpletable_DF1914FD351E4F2BA61372A52F0CFFBF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> profile</span></span> </p></td> 
  <td class="stentry"> <p>ICCカラープロファイル。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent  </span> </span> </p></td> 
  <td class="stentry"> <p>知覚の |相対 |彩度 | absolute </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span> </span> </p></td> 
  <td class="stentry"> <p>1は有効に、0は黒点補正を無効にします。 </p></td> 
 </tr> 
</table>

*`profile`* は、作業プロファイルと異なる場合にレンダリングイメージを変換する出力カラースペースプロファイルを指定します。*`profile`* は、画像カタログまたはデ `icc::Name` フォルトカタログのICCプロファイルマップで定義されている有効なパス、またはプロファイルファイルの相対パス（通常は、またはサフィックスを持つ） [!DNL .icc]である必 [!DNL .icm] 要があります。

>[!NOTE]
>
>*`profile`* は、HTTPエンコードされている場合でも、「,」文字を含めることはできません。

*`renderIntent`* デフォルトのレンダリングインテントを上書きできます。

*`blackpointComp`* 出力プロファイルがこの機能をサポートしている場合、ブラックポイント補正を有効にします。

>[!NOTE]
>
>すべての&#x200B;*`renderIntent`*&#x200B;と&#x200B;*`blackpointComp`*&#x200B;の選択肢がカラー変換でサポートされているわけではありません。 通常、これらの設定は、ICC出力プロファイルがプリンターやモニターなどの出力デバイスを特徴付ける場合にのみ有効です。 また、一部のICC出力プロファイルは&#x200B;*`renderIntent`*&#x200B;の選択肢をサポートしていません。

## プロパティ {#section-b4042623a8ea40248c11b2153e5906b1}

リクエスト内の任意の場所で発生する可能性があります。 画像タイプが`fmt=`で指定されている場合、*`profile`*&#x200B;と一致しないとエラーが返されます。

*`renderIntent`* および *`blackpointComp`* は、指定されたICCプロファイルと互換性がない場合は無視されます。

CMYK出力デバイスプロファイルは、様々なレンダリング意図をサポートする可能性が高くなります。

## 初期設定 {#section-bbd3206fdcac4dc48a08fc9eba14fc90}

カラーマネジメントが有効で`icc=`が指定されていない場合、サーバーは`fmt=`で指定された画像タイプに一致する出力プロファイル(`attribute::IccProfile*`)に変換された画像を配信します。

指定しなかった場合、*`renderIntent`*&#x200B;は`attribute::IccRenderIntent`から継承され、*`blackpointComp`*&#x200B;は`attribute::IccBlackPointCompensation`から継承されます。

## 関連項目 {#section-37ef83149fd74345956a98f633cc0294}

[カラーマネジメント](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-color-management.md#concept-7bac7c2c41be42c1b301eae80abe6b8d)、 [attribute::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127)、 [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f)、 [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)、 [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)、 [attribute::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0)
