---
description: 出力カラープロファイル
seo-description: 出力カラープロファイル
seo-title: icc
solution: Experience Manager
title: icc
topic: Scene7 Image Serving - Image Rendering API
uuid: 95a05fe5-d6b3-4118-aab4-4664ccee2850
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# icc{#icc}

出力カラープロファイル

icc= *`profile`*[, *`renderIntent`*[,*`blackpointComp`*]]

<table id="simpletable_DF1914FD351E4F2BA61372A52F0CFFBF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 輪郭</span></span> </p></td> 
  <td class="stentry"> <p>ICCカラープロファイル。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> レンダリ <span class="varname"> ングインテ </span> ント </span> </p></td> 
  <td class="stentry"> <p>知覚の|相対|彩度|絶対 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span></span> </p></td> 
  <td class="stentry"> <p>1を指定すると有効になり、0を指定するとブラックポイントの補正が無効になります。 </p></td> 
 </tr> 
</table>

*`profile`* 作業プロファイルと異なる場合にレンダリングイメージを変換する出力カラースペースプロファイルを指定します。 *`profile`* は、画像カタログのICCプ `icc::Name` ロファイルマップまたは初期設定のカタログで定義された有効なパス、またはプロファイルファイルの相対パス(通常は、サフィックス付きまたはサ [!DNL .icc]フィッ [!DNL .icm] クス付き)です。

>[!NOTE]
>
>*`profile`* は、HTTPエンコードされている場合でも、「,」文字を含めることはできません。

*`renderIntent`* 初期設定のレンダリングインテントを上書きできます。

*`blackpointComp`* 出力プロファイルがこの機能をサポートしている場合、ブラックポイントの補正を有効にします。

>[!NOTE]
>
>すべての色変換が、選択肢をサポートしてい *`renderIntent`* るわけでは *`blackpointComp`* ありません。 通常、これらの設定は、ICC出力プロファイルがプリンターやモニターなどの出力デバイスの特性を示す場合にのみ適用されます。 また、一部のICC出力プロファイルでは、選択肢の一部がサポートされて *`renderIntent`* いません。

## プロパティ {#section-b4042623a8ea40248c11b2153e5906b1}

リクエスト内の任意の場所で発生する可能性があります。 で指定された画像タイプが一致しない場合は、エ `fmt=` ラーが返されま *`profile`*&#x200B;す。

*`renderIntent`* とは、指 *`blackpointComp`* 定したICCプロファイルと互換性がない場合は無視されます。

CMYK出力デバイスプロファイルは、様々なレンダリングインテントをサポートする可能性が高くなります。

## 初期設定 {#section-bbd3206fdcac4dc48a08fc9eba14fc90}

カラーマネジメントが有効で、指定さ `icc=` れていない場合、サーバは、で指定された画像タイプに一致する出力プロファイル( `attribute::IccProfile*`)に変換された画像を配信しま `fmt=`す。

指定しなかった場合、は *`renderIntent`* から継承され、 `attribute::IccRenderIntent`はから *`blackpointComp`* 継承されます `attribute::IccBlackPointCompensation`。

## 関連項目 {#section-37ef83149fd74345956a98f633cc0294}

[Color Management,](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-color-management.md#concept-7bac7c2c41be42c1b301eae80abe6b8d)attribute:IccProfile, [iccEmbed=](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127), [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f), ffmt= [](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)[](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)[,*Attribute:Icc Render IntentIntentAttribute:Icc Render IntentAttribute:IccBlackPoint Compensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0)
