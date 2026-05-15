---
title: 量子化
description: カラーの量子化： GIF出力変換のカラー量子化属性を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71d59961-848e-4d78-875e-066e842ac1bf
TQID: 'https://experienceleague.adobe.com/gQ4YOSwrnbp0uNqQzC-aexuXaU9DZwQHXz3PdfaTaV0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 237
ht-degree: 1%

---

# 量子化{#quantize}

カラーの量子化： GIF出力変換のカラー量子化属性を指定します。

` quantize= *`type`*[, *`dither`*[, *`numColors`*[, *`colorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> タイプ </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac} </span> </p> <p>パレットの種類を指定します。 </p> <p>画像に最適なパレットを計算するには、<span class="codeph"> アダプティブ </span>に設定します。 </p> <p>事前定義済みのパレットを選択するには、<span class="codeph"> web </span>または<span class="codeph"> mac </span>に設定します。 </p> <p> <p>注意：<span class="codeph"> mac </span> パレットの種類は、GIFおよびPNG8 フォーマットでのみサポートされますが、GIF AlphaおよびPNG8-Alpha フォーマットではサポートされていません。</p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ディザ </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {diffuse|off} </span> </p> <p>ディザリングオプションを指定します。 </p> <p>Floyd-Steinberg エラー拡散の拡散を<span class="codeph">拡散</span>に設定 </p> <p>ディザリングを無効にするには、</span>から<span class="codeph">に設定します。</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
   <td colname="col2"> <p>出力カラー数（2 ～ 256） </p> <p><span class="codeph"> アダプティブ </span> パレットに含まれるカラーの数を指定します。</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> colorList </span> </span> </p> </td> 
   <td colname="col2"> <p>16進数6形式の強制RGB カラーのコンマ区切りリスト </p> <p><span class="codeph"> アダプティブ </span> パレットに含める色を指定できます。 指定されたカラー数が<span class="codeph"> <span class="varname"> numColors </span> </span>未満の場合、追加のカラーは画像コンテンツに基づいて計算されます。</p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-8ab5035055b24b858270d260912a7f3d}

リクエスト属性： 現在のレイヤー設定に関係なく適用されます。 `fmt=gif`、`fmt=gif-alpha`、`fmt=png8`、または`fmt=png8-alpha`の場合にのみ使用されます。 それ以外は無視されます。

*`colorList`*&#x200B;で指定されたカラーは、16進数6のRGB値で構成されている必要があります（`0x`接頭辞のない[color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md)を参照）。 他のカラー指定子は使用できません。 修飾子&#x200B;*`numColors`*&#x200B;は2 ～ 256である必要があります。

## 初期設定 {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## 例 {#section-e34aca7587d548a7ae9d4266b80c9451}

`web` パレットを使用してGIF サムネールを生成し、ディザリングを行いません。

`http:// *`*サーバー*`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

キーカラーの透明度を使用して、画像をバイトーンのGIFに変換します。 また、カラーを白黒に強制します。

`http:// *`*サーバー*`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## 関連項目 {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)、[color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
