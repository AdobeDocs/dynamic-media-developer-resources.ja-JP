---
description: 色量子化。 GIF出力変換のカラー量子化属性を指定します。
seo-description: 色量子化。 GIF出力変換のカラー量子化属性を指定します。
seo-title: 量子化する
solution: Experience Manager
title: 量子化する
topic: Scene7 Image Serving - Image Rendering API
uuid: 4e9c4807-59bc-4eb9-bcab-0bf0cfdf56d4
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 3%

---


# 量子化{#quantize}

色量子化。 GIF出力変換のカラー量子化属性を指定します。

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorscolorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac}  </span> </p> <p>パレットの種類を指定します。 </p> <p>画像に最適なパレットを計算するには、<span class="codeph">アダプティブ</span>に設定します。 </p> <p><span class="codeph"> web </span>または<span class="codeph"> mac </span>に設定すると、定義済みのパレットを選択できます。 </p> <p> <p>注意： <span class="codeph"> mac </span>パレットタイプは、GIFおよびPNG8形式でのみサポートされますが、GIF-AlphaおよびPNG8-Alpha形式ではサポートされません。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ディザ  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {diffuse|off}  </span> </p> <p>ディザリングオプションを指定します。 </p> <p>Floyd-Steinberg誤差拡散用に<span class="codeph"> diffuse </span>に設定 </p> <p>ディザリングを無効にするには、<span class="codeph"> off </span>に設定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> </p> </td> 
   <td colname="col2"> <p>出力色の数(2 ～ 256) </p> <p><span class="codeph">アダプティブ</span>パレットに含める色の数を指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> colorList  </span> </span> </p> </td> 
   <td colname="col2"> <p>強制のRGBカラーを16進数6形式でカンマ区切りしたリスト </p> <p><span class="codeph">アダプティブ</span>パレットに含める色を指定できます。 指定した色の数が<span class="codeph"> <span class="varname"> numColors </span> </span>より少ない場合、画像の内容に基づいて追加の色が計算されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-8ab5035055b24b858270d260912a7f3d}

要求属性。 現在のレイヤー設定に関係なく適用されます。 `fmt=gif`、`fmt=gif-alpha`、`fmt=png8`、または`fmt=png8-alpha`の場合にのみ使用されます。 それ以外の場合は無視されます。

` *`colorList`*`で指定する色は、16進数6形式のRGB値（`0x`を参照）で構成され、プレフィックスは付けません。 ` [color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423)`他の色指定子は使用できません。 *`numColors`* は2 ～ 256の範囲で設定する必要があります。

## 初期設定 {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## 例 {#section-e34aca7587d548a7ae9d4266b80c9451}

`web`パレットを使用し、ディザリングなしでGIFサムネールを生成します。

` http:// *`server`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

キーカラーの透明部分を持つバイトナルGIFに画像を変換し、カラーを白黒に強制的に変換します。

` http:// *`server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## 関連項目 {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ,  [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
