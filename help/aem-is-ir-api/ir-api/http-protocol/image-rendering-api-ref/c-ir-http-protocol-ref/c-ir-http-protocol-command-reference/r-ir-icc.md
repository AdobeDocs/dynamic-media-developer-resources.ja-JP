---
title: icc
description: 出力カラープロファイル。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39b25f7c-ed3c-4132-8241-e7f3aab07b00
TQID: 'https://experienceleague.adobe.com/vC889xf6GmyiSls7qG81NPIegfh6OMZM2zMc4JKppAU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 235
ht-degree: 1%

---

# icc{#icc}

出力カラープロファイル。

icc= *`profile`*[, *`renderIntent`*[,*`blackpointComp`*]]

<table id="simpletable_DF1914FD351E4F2BA61372A52F0CFFBF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> プロファイル </span></span> </p></td> 
  <td class="stentry"> <p>ICC カラープロファイル。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent </span> </span> </p></td> 
  <td class="stentry"> <p>知覚的|相対|彩度|絶対 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span> </span> </p></td> 
  <td class="stentry"> <p>1を有効にする場合は0、ブラックポイントの補償を無効にする場合は0。 </p></td> 
 </tr> 
</table>

*`profile`* レンダリングされた画像が作業用プロファイルと異なる場合に、変換する出力色空間プロファイルを指定します。*`profile`* 画像カタログまたはデフォルトカタログのICC プロファイルマップで定義された有効な`icc::Name`か、プロファイルファイルへの相対パス（通常は[!DNL `.icc`]または[!DNL `.icm`]接尾辞）である必要があります。

>[!NOTE]
>
>*`profile`*&#x200B;は、HTTP エンコードされた場合でも、「,」文字を含めることはできません。

*`renderIntent`*&#x200B;既定のレンダリング インテントを上書きできます。

*`blackpointComp`*&#x200B;出力プロファイルがこの機能をサポートしている場合、ブラックポイント補正を有効にします。

>[!NOTE]
>
>すべてのカラーコンバージョンが&#x200B;*`renderIntent`*&#x200B;と&#x200B;*`blackpointComp`*&#x200B;のすべての選択肢をサポートしているわけではありません。 通常、これらの設定は、ICC出力プロファイルがプリンターやモニターなどの出力デバイスを特徴付ける場合にのみ適用されます。 また、一部のICC出力プロファイルは、すべての&#x200B;*`renderIntent`*&#x200B;の選択肢をサポートしていません。

## プロパティ {#section-b4042623a8ea40248c11b2153e5906b1}

リクエスト内のどこでも発生する可能性があります。 画像の種類が`fmt=`で指定されている場合、*`profile`*&#x200B;と一致しない場合は、エラーが返されます。

指定されたICC プロファイルと互換性がない場合、*`renderIntent`*&#x200B;と&#x200B;*`blackpointComp`*&#x200B;の両方が無視されます。

CMYK出力デバイスプロファイルは、異なるレンダリングインテントをサポートする可能性が高くなります。

## 初期設定 {#section-bbd3206fdcac4dc48a08fc9eba14fc90}

カラーマネジメントが有効で`icc=`が指定されていない場合、サーバーは、指定した画像タイプと`fmt=`が一致する出力プロファイル （`attribute::IccProfile*`）に変換された画像を配信します。

指定しない場合、*`renderIntent`*&#x200B;は`attribute::IccRenderIntent`から継承され、*`blackpointComp`*&#x200B;は`attribute::IccBlackPointCompensation`から継承されます。

## 関連項目 {#section-37ef83149fd74345956a98f633cc0294}

[ カラーマネジメント ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-color-management.md#concept-7bac7c2c41be42c1b301eae80abe6b8d)、[属性：:IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127)、[iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f)、[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)、[属性：:IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)、[属性：:IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0)
