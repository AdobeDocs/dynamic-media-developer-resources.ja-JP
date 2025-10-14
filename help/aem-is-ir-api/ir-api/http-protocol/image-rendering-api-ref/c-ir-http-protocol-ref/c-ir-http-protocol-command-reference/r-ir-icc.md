---
title: icc
description: 出力カラープロファイル。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39b25f7c-ed3c-4132-8241-e7f3aab07b00
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 1%

---

# icc{#icc}

出力カラープロファイル。

icc= *`profile`*[, *`renderIntent`*[,*`blackpointComp`*]]

<table id="simpletable_DF1914FD351E4F2BA61372A52F0CFFBF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> profile</span></span> </p></td> 
  <td class="stentry"> <p>ICC カラープロファイル。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent </span> </span> </p></td> 
  <td class="stentry"> <p>知覚的 |相対 |彩度 |絶対パス </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span> </span> </p></td> 
  <td class="stentry"> <p>1 を有効にするには、0 を指定するとブラックポイント補正が無効になります。 </p></td> 
 </tr> 
</table>

*`profile`* レンダリング イメージが作業プロファイルと異なる場合に変換される出力カラースペース プロファイルを指定します。 *`profile`* 有効な `icc::Name` は、画像カタログの ICC プロファイルマップまたはデフォルトカタログで定義されているか、プロファイルファイルへの相対パス（通常は [!DNL `.icc`] または [!DNL `.icm`] サフィックスを含む）である必要があります。

>[!NOTE]
>
>*`profile`* HTTP でエンコードされている場合でも、「,」文字を含めることはできません。

*`renderIntent`* デフォルトのレンダリングインテントを上書きできます。

*`blackpointComp`* 出力プロファイルがこの機能をサポートしている場合は、ブラックポイント補正を有効にします。

>[!NOTE]
>
>すべてのカラー変換ですべての *`renderIntent`* および *`blackpointComp`* の選択がサポートされているわけではありません。 通常、これらの設定は、ICC 出力プロファイルがプリンターやモニターなどの出力デバイスを特徴付ける場合にのみ適用されます。 また、一部の ICC 出力プロファイルは、*`renderIntent`* の選択肢の一部をサポートしていません。

## プロパティ {#section-b4042623a8ea40248c11b2153e5906b1}

は、リクエスト内のどこでも発生する可能性があります。 `fmt=` で指定された画像タイプが *`profile`* と一致しない場合、エラーが返されます。

指定された ICC プロファイルと互換性がない場合、*`renderIntent`* と *`blackpointComp`* の両方は無視されます。

CMYK 出力デバイスプロファイルは、異なるレンダリングインテントをサポートする可能性が高くなります。

## 初期設定 {#section-bbd3206fdcac4dc48a08fc9eba14fc90}

カラーマネジメントが有効になっていて、`icc=` が指定されていない場合、サーバーは `attribute::IccProfile*` で指定された画像タイプに一致する画像を出力プロファイル（`fmt=`）に変換して配信します。

指定しない場合、*`renderIntent`* は `attribute::IccRenderIntent` から、*`blackpointComp`* は `attribute::IccBlackPointCompensation` から継承されます。

## 関連項目 {#section-37ef83149fd74345956a98f633cc0294}

[&#x200B; カラーマネジメント &#x200B;](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-color-management.md#concept-7bac7c2c41be42c1b301eae80abe6b8d), [attribute::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127), [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f), [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0)
