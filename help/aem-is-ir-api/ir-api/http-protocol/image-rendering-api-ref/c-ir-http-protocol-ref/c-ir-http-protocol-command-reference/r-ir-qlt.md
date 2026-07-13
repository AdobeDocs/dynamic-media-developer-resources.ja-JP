---
title: qlt
description: Jpeg品質： 圧縮レベルを制御するためのJPEG エンコーディング属性を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 49af2620-081f-4bcc-8245-5aa6bab89a05
TQID: 'https://experienceleague.adobe.com/T-e5oTA39GatOq7DkXIZPelLxnudZe3O1JYX0bOwlXk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 201
ht-degree: 6%

---

# qlt{#qlt}

Jpeg品質： 圧縮レベルを制御するためのJPEG エンコーディング属性を指定します。

` qlt= *`品質`*[. *` クロマ `*]`

<table id="simpletable_A245B6A3D2374A6A89DE63A5621CFEC0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">品質</span> </p> </td> 
  <td class="stentry"> <p>JPEG エンコーディングの品質（1...100） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> クロマ </span> </p> </td> 
  <td class="stentry"> <p>JPEGの色度ダウンサンプリング（0=標準、1=無効）。オプション、デフォルトは0です。 </p> </td> 
 </tr> 
</table>

圧縮レベルを制御するためのJPEG エンコーディング属性を指定します。 これにより、ファイルサイズ（返信データの量）、間接的に結果の画像の視覚的な画質が変化します。

*`quality`*&#x200B;値を大きくすると、ファイルサイズと画質が大きくなり、値を小さくすると、ファイルサイズが小さくなり、画像の質が低下します。 90 を超える値を指定すると、一般的には非圧縮画像と区別がつかないほどの画像が生成されます。

*`chroma`* フラグを設定して、一般的なJPEG エンコーダで使用される色度のダウンサンプリングを無効にします。 この設定は、エッジが明るさではなく色相の変化によって定義される場合に、画像内のエッジのシャープを増幅する場合があります。 このフラグを設定すると、ファイルサイズが若干増加する場合があります。 テキストが少しぼやけている場合は、この設定を試してください。

## プロパティ {#section-897b61c786dd4230a2c5807f2f40e722}

リクエスト内のどこでも発生する可能性があります。

出力イメージのフォーマットがJPEG圧縮をサポートしていない場合は無視されます。 JPEG圧縮をサポートする出力画像フォーマットの一覧については、`fmt=`の説明を参照してください。

## 初期設定 {#section-1c1257df843c475bbac6aadaffcb6347}

`attribute::JpegQuality`

## 関連項目 {#section-61871fbded3a42f68cf3bdcaed35eae1}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)、[属性：:JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50)

