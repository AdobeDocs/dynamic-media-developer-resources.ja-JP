---
title: 量子化
description: カラー量子化。 GIFの出力変換に使用するカラー量子化属性を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71d59961-848e-4d78-875e-066e842ac1bf
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 1%

---

# 量子化{#quantize}

カラー量子化。 GIFの出力変換に使用するカラー量子化属性を指定します。

` quantize= *`type`*[, *`dither`*[, *`numColors`*[, *`colorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac} </span> </p> <p>パレットの種類を指定します。 </p> <p>をアダプティブフ </span> ーム <span class="codeph"> 設定して、画像に最適なパレットを計算します。 </p> <p>Web </span> または <span class="codeph"> mac </span> に設定 <span class="codeph"> て、事前定義済みのパレットを選択します。 </p> <p> <p>注：<span class="codeph"> mac </span> のパレットタイプは、GIF形式と PNG8 形式でのみサポートされており、GIFAlpha形式と PNG8Alpha形式ではサポートされていません。</p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> dither </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {diffuse|off} </span> </p> <p>ディザリングオプションを指定します。 </p> <p>Floyd-Steinberg 誤差拡散 <span class="codeph"> 拡散 </span> に設定します </p> <p><span class="codeph"> off </span> に設定すると、ディザリングが無効になります。</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
   <td colname="col2"> <p>出力色数（2～256） </p> <p><span class="codeph"> アダプティブフ </span> ームパレットに含める色の数を指定します。</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> colorList </span> </span> </p> </td> 
   <td colname="col2"> <p>16 進数 6 形式の強制RGBカラーのコンマ区切りリスト </p> <p><span class="codeph"> アダプティブフ </span> ームパレットに含めるカラーを指定できます。 指定した色の数が numColors または </span> の <span class="codeph"> より少ない場合 <span class="varname">、画像 </span> 内容に基づいて追加の色が計算されます。</p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-8ab5035055b24b858270d260912a7f3d}

リクエスト属性。 現在のレイヤ設定に関係なく適用されます。 `fmt=gif`、`fmt=gif-alpha`、`fmt=png8` または `fmt=png8-alpha` の場合にのみ使用されます。 それ以外の場合は無視されます。

*`colorList`* で指定するカラーは、16 進数 6 形式のRGB値（[color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md) でプレフィックスのない値で構成されてい `0x` 必要があります。 他の色指定子は使用できません。 修飾子 *`numColors`* は 2 ～ 256 にする必要があります。

## 初期設定 {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## 例 {#section-e34aca7587d548a7ae9d4266b80c9451}

`web` パレットを使用し、ディザリングを行わずにGIFのサムネールを生成します。

`http:// *`*サーバー*`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

キーカラーの透明度を持つ双色調のGIFに画像を変換します。 また、カラーを白黒に強制します。

`http:// *`*サーバー*`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## 関連項目 {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
