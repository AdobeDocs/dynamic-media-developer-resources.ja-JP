---
description: カラー量子化。 GIF出力変換のカラー量子化属性を指定します。
solution: Experience Manager
title: 量子化する
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 71d59961-848e-4d78-875e-066e842ac1bf
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 3%

---

# 量子化する{#quantize}

カラー量子化。 GIF出力変換のカラー量子化属性を指定します。

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorscolorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac}  </span> </p> <p>パレットの種類を指定します。 </p> <p><span class="codeph">アダプティブ</span>に設定すると、画像に最適なパレットが計算されます。 </p> <p><span class="codeph"> web </span>または<span class="codeph"> mac </span>に設定すると、事前定義済みのパレットを選択できます。 </p> <p> <p>注意： <span class="codeph"> mac </span>のパレットタイプは、GIFおよびPNG8形式に対してのみサポートされますが、GIF-AlphaおよびPNG8-Alpha形式に対してはサポートされません。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ディザ  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {diffuse|off}  </span> </p> <p>ディザリングオプションを指定します。 </p> <p>Floyd-Steinberg誤差拡散用に<span class="codeph">拡散</span>に設定 </p> <p><span class="codeph"> off </span>に設定すると、ディザリングが無効になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> </p> </td> 
   <td colname="col2"> <p>出力色の数(2～256) </p> <p><span class="codeph">アダプティブ</span>パレットに含める色の数を指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> colorList  </span> </span> </p> </td> 
   <td colname="col2"> <p>強制されたRGBカラーの16進数6形式のコンマ区切りリスト </p> <p><span class="codeph">アダプティブ</span>パレットに含める色を指定できます。 指定した色数が<span class="codeph"> <span class="varname"> numColors </span> </span>未満の場合、画像の内容に基づいて追加の色が計算されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-8ab5035055b24b858270d260912a7f3d}

リクエスト属性。 現在の画層設定に関係なく適用されます。 `fmt=gif`、`fmt=gif-alpha`、`fmt=png8`、または`fmt=png8-alpha`の場合にのみ使用されます。 それ以外の場合は無視されます。

`*`colorList`*`で指定する色は、プレフィックス「`0x`」を付けずに、16進数6形式のRGB値で構成する必要があります（` [color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423)`を参照）。 他の色指定子は使用できません。 *`numColors`* は2 ～ 256の範囲で設定する必要があります。

## 初期設定 {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## 例 {#section-e34aca7587d548a7ae9d4266b80c9451}

`web`パレットを使用し、ディザリングを使用せずにGIFサムネールを生成します。

` http:// *`server`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

キーカラーの透明度とカラーを白黒に強制的に設定して、画像をバイトナルGIFに変換します。

` http:// *`server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## 関連項目 {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ,  [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
